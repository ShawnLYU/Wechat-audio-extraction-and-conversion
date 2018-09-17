# wechat_audio_conversion

This integrates tools and knowledges to convert wechat audio into mp3 format for storage purpose (MacOS).


## Getting Started

For simplicity, the whole process will be shown as below.

### Prerequisites

[Homebrew](https://brew.sh/)

### Deplyment

Say what the steps will be


* Install [FFmpeg](https://www.ffmpeg.org/)
Homebrew is recommended for installation
```
brew install ffmpeg --with-libvpx
```
* Install [silk-v3-decoder](https://github.com/kn007/silk-v3-decoder)
```
git clone https://github.com/kn007/silk-v3-decoder.git
```
* Locate the route for certain audio message on your Mac
You may convert audio messages ether from dialogues or from your [favorite](https://chinachannel.co/wechat-favorites-free-1g-of-cloud-storage-wechat-essential-tips/)
When you navigate to 
```
/Users/username/Library/Containers/com.tencent.xinWeChat/Data/Library/Application Support/com.tencent.xinWeChat/2.0b4.0.9
```
you will see one or more encoded string, each of which stands for an account that has been logged into your machine. Try figuring which one is your account(you are on your own this time).
Then you may navigete into it and select ether Favorites or Message, and following the route you will get to see the [silk](https://en.wikipedia.org/wiki/SILK) files, which are the files we will convert thereafter.

* Start converting
Learning from [kn007](https://github.com/kn007), you may:
** Convert one file at a time
```
sh converter.sh silk_v3_file/input_folder output_format/output_folder flag(format)
```
or
** Convert in batches
```
sh converter.sh input ouput mp3
```

## Acknowledgments

* [kn007]https://github.com/kn007

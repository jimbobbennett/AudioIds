# Audio Ids

This is a macOS tool to get the Device UIDs of all the microphones connected to your Mac.

You can use the output device UIDs to configure the audio config for the [Azure cognitive services speech SDK](https://docs.microsoft.com/azure/cognitive-services/speech-service/how-to-select-audio-input-devices/?WT.mc_id=audioids-github-jabenn).

For example - with this output:

```sh
2019-06-28 17:07:29.682992+0100 AudioIds[55558:3491097] {
    deviceName = "Built-in Microphone";
    deviceUID = "AppleHDAEngineInput:1F,3,0,1,0:1";
}
2019-06-28 17:07:29.683729+0100 AudioIds[55558:3491097] {
    deviceName = "USB Advanced Audio Device";
    deviceUID = "AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2";
}
2019-06-28 17:07:29.683767+0100 AudioIds[55558:3491097] {
    deviceName = "Logitech Webcam C930e";
    deviceUID = "AppleUSBAudioEngine:Unknown Manufacturer:Logitech Webcam C930e:FBA21F8E:3";
}
```Program ended with exit code: 0
```

If you wanted to use the **USB Advanced Audio Device** you would set the the audio config to `"AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2"`.

## C++

```cpp
audioConfig = AudioConfig.FromMicrophoneInput("AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2");
```

## C#

```cs
audioConfig = AudioConfig.FromMicrophoneInput("AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2");
```

## Python

```python
audio_config = AudioConfig(device_name="AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2");
```

## Objective-C

```objc
audioConfig = AudioConfiguration.FromMicrophoneInput("AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2");
```

## Java

```java
audioConfig = AudioConfiguration.fromMicrophoneInput("AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2");
```

## JavaScript

```js
audioConfig = AudioConfiguration.fromMicrophoneInput("AppleUSBAudioEngine:C-Media Electronics Inc.:USB Advanced Audio Device:14431100:2");
```

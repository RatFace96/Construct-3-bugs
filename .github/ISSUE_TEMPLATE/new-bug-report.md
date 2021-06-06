---
name: RemotePreviewCrash
about: Entire project crashes when using construct 3's remote preview feature via chrome.
title: 'Crash'
labels: 'remote preview'
assignees: ''

---

<!-- You must use this template or your issue will be closed without investigation. Please see the guidelines. -->

## Problem description

Project crashes when using construct 3's remote preview feature via Chrome. Happens once the other person tries to connect. Happens with every project file I make, but I've attached one to follow the guidelines.

## Attach a .c3p

https://drive.google.com/file/d/1q0STiVYaujOpHeAUl0n52wIMEdjUMkua/view?usp=sharing

## Steps to reproduce

1. Open Project from Chrome, Windows (use chrome as host)
2. Start Remote preview
3. Connect via Safari, iPadOS (However, same happens if connecting from Chrome, iPadOS/Chrome, Windows(from a different device)/Firefox, Windows

## Observed result

Crashes once the link is opened.
Screenshot: https://user-images.githubusercontent.com/63507734/120940388-5345e280-c71d-11eb-82cc-7602c05ae93d.png

## Expected result

For remote preview to work

## More details
<!-- Providing this information will make it more likely the issue you are reporting can be fixed quickly. -->
When hosting from Safari, iPadOS:
Chrome didn't crash but instead said:
Error: TypeError: RTCPeerConnection is not a constructor
Screenshot: https://user-images.githubusercontent.com/63507734/120941142-635fc100-c721-11eb-9e0a-6f381b7fa0ad.png

Whereas Whereas it opened fine on Firefox, Windows.

When hosting from Firefox, Windows:
Chrome simply said:
Error: join-failed
Screenshot: https://user-images.githubusercontent.com/63507734/120941355-948cc100-c722-11eb-81e8-233a419da5b9.png

Whereas it opened fine on Safari, iPadOS.

<!-- It's helpful to test as many browsers, platforms or export options as possible. For example an issue occurs in an Android app, does it also occur in Chrome on Windows? How about Firefox? etc. -->

**Affected browsers/platforms:** <!-- Chrome/Firefox/Safari, Windows/macOS/Android, etc -->

Chrome, Windows as host or receipient

**First affected release:** <!-- e.g. worked in r122 but broke in r123 -->

R241 (but has been broken since I started using C3 about 3 months ago?)

## System details

<!-- If you see a crash report dialog, please copy and paste it to where it says "PASTE HERE" below. -->
<!-- Otherwise please go to Menu > About > Platform information and paste that information there instead. -->

The below system details are from the initial scenario of hosting from Chrome, Windows and opening the link on Safari, iPadOS
Screenshot: https://user-images.githubusercontent.com/63507734/120940388-5345e280-c71d-11eb-82cc-7602c05ae93d.png
<details><summary>View details</summary>

Error report information
Type: unhandled rejection
Reason: Error: d is not a constructor @ TypeError: d is not a constructor at self.GHa.zra (https://editor.construct.net/r241/exporters/preview/exporter.js:24:397) at self.f1b.hkd (https://editor.construct.net/r241/exporters/preview/exporter.js:39:434) at self.eWc.Gpb.hF.oeb (https://editor.construct.net/r241/exporters/preview/exporter.js:38:40) at self.eWc.Twa (https://editor.construct.net/r241/exporters/preview/exporter.js:18:301) at WebSocket.WT.onmessage (https://editor.construct.net/r241/exporters/preview/exporter.js:16:269)
Stack: TypeError: d is not a constructor at self.GHa.zra (https://editor.construct.net/r241/exporters/preview/exporter.js:24:397) at self.f1b.hkd (https://editor.construct.net/r241/exporters/preview/exporter.js:39:434) at self.eWc.Gpb.hF.oeb (https://editor.construct.net/r241/exporters/preview/exporter.js:38:40) at self.eWc.Twa (https://editor.construct.net/r241/exporters/preview/exporter.js:18:301) at WebSocket.WT.onmessage (https://editor.construct.net/r241/exporters/preview/exporter.js:16:269)
Construct 3 version: r241
URL: https://editor.construct.net/
Date: Sun Jun 06 2021 23:17:07 GMT+0200 (Eastern European Standard Time)
Uptime: 1053.2 s

Platform information
Browser: Chrome
Browser version: 91.0.4472.77
Browser engine: Chromium
Browser architecture: 64-bit
Context: browser
Operating system: Windows
Operating system version: 10
Operating system architecture: 64-bit
Device type: desktop
Device pixel ratio: 1.100000023841858
Logical CPU cores: 12
Approx. device memory: 8 GB
User agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.77 Safari/537.36
C3 release: r241 (stable)
Language setting: en-US

WebGL information
Version string: WebGL 2.0 (OpenGL ES 3.0 Chromium)
Numeric version: 2
Supports NPOT textures: yes
Supports GPU profiling: yes
Supports highp precision: yes
Vendor: Google Inc. (NVIDIA)
Renderer: ANGLE (NVIDIA, NVIDIA GeForce GTX 1050 Ti Direct3D11 vs_5_0 ps_5_0, D3D11-27.21.14.6663)
Major performance caveat: no
Maximum texture size: 16384
Point size range: 1 to 1024
Extensions: EXT_color_buffer_float, EXT_color_buffer_half_float, EXT_disjoint_timer_query_webgl2, EXT_float_blend, EXT_texture_compression_bptc, EXT_texture_compression_rgtc, EXT_texture_filter_anisotropic, EXT_texture_norm16, KHR_parallel_shader_compile, OES_texture_float_linear, WEBGL_compressed_texture_s3tc, WEBGL_compressed_texture_s3tc_srgb, WEBGL_debug_renderer_info, WEBGL_debug_shaders, WEBGL_lose_context, WEBGL_multi_draw, OVR_multiview2

</details>

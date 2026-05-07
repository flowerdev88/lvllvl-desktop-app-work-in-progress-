# NW.js with Apache & PHP

![NW.js](https://img.shields.io/badge/NW.js-v0.75.0-blue) ![Apache](https://img.shields.io/badge/Apache-2.4.63-green) ![PHP](https://img.shields.io/badge/PHP-8.4.4-blueviolet)

NW.js with Apache & PHP is a mod for NW.js that allows you to run an Apache server and PHP in the background. On startup, it opens `index.html`, redirects to `index.php`, and displays the rendered page in NW.js's Chromium browser.

This setup uses:
- **Apache 2.4.63-250207-win64**
- **PHP 8.4.4-Win32-vs17-x64**

---

## Features
- Starts Apache and PHP automatically in the background.
- Opens `index.html` on load, then redirects to `index.php`.
- Displays the rendered PHP page in NW.js's Chromium browser.
- Supports video/audio playback (requires FFmpeg).

---

## Requirements

### Mandatory
1. **NW.js Windows 64-bit**  
   Download the SDK version if you want access to DevTools:  
   [NW.js Downloads](https://nwjs.io/downloads/)

2. **Microsoft Visual C++ Redistributable**  
   Required for running Apache and PHP:  
   [Download VC++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe)

### Optional
- **FFmpeg Prebuilt Binaries for NW.js**  
   If you want to play videos or audio, download FFmpeg prebuilt binaries and place `ffmpeg.dll` inside the NW.js folder (where `nw.exe` is located).  
   [FFmpeg for NW.js](https://github.com/nwjs-ffmpeg-prebuilt/nwjs-ffmpeg-prebuilt)

---

## Installation

1. **Download NW.js**  
   Download the Windows 64-bit SDK version of NW.js from the official website:  
   [NW.js Downloads](https://nwjs.io/downloads/)

2. **Install Microsoft Visual C++ Redistributable**  
   Install the latest version of the Microsoft Visual C++ Redistributable:  
   [Download VC++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe)

3. **Add FFmpeg (Optional)**  
   If you need video/audio support, download FFmpeg prebuilt binaries for NW.js and place `ffmpeg.dll` in the NW.js folder (where `nw.exe` is located).

4. **Upload `package.nw`**   
   - Place the `package.nw` folder/directory inside the NW.js folder (where `nw.exe` is located).

5. **Run NW.js**  
   Launch `nw.exe` to start the application. Apache and PHP will start automatically in the background, and the app will open `index.html`, redirecting to `index.php`.

---

## Usage

- The application will automatically start Apache and PHP when launched.
- It will open `index.html`, which redirects to `index.php`.
- The rendered PHP page will be displayed in NW.js's Chromium browser.

---

## Notes

- Ensure that no other service is using port `80` (default Apache port). If port `80` is occupied, modify the Apache configuration to use a different port.
- If you encounter issues with PHP not working, verify that the PHP binaries are correctly configured in the Apache settings.
- For development purposes, you can enable DevTools by downloading the SDK version of NW.js.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Credits

- **NW.js**: [https://nwjs.io/](https://nwjs.io/)
- **Apache HTTP Server**: [https://httpd.apache.org/](https://httpd.apache.org/)
- **PHP**: [https://www.php.net/](https://www.php.net/)
- **FFmpeg for NW.js**: [https://github.com/nwjs-ffmpeg-prebuilt/nwjs-ffmpeg-prebuilt](https://github.com/nwjs-ffmpeg-prebuilt/nwjs-ffmpeg-prebuilt)

---

Feel free to contribute or report issues!  
Happy coding! 🚀

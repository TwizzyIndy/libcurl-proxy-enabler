# libcurl proxy enabler
[CURL](https://curl.se/) lib is using it's own proxy. So, it will be difficult to intercept HTTP(S) calls on Windows using some http proxy tools. I decided to hook the export calls for the target app using [FRIDA](https://frida.re). Then it was happen. Some basic `frida-tools` should be installed on the PC. [Frida Installation](https://frida.re/docs/installation/)

## Usage
```bash
npm install
frida -n SomeApp.exe -l index.js
```
[![Homebrew SD Setup](https://www.sdsetup.com/img/logo.png)](https://www.sdsetup.com)

[https://www.sdsetup.com](https://www.sdsetup.com)

Homebrew SD Setup is a web application written in C# (and a little bit of JavaScript) running on Blazor. The app lets you select the homebrew applications and custom firmwares you want, and quickly create a zip archive to extract to your SD card. The Ninite for your game consoles.

## Compatibility
The application has been verified working in Chrome, Firefox, Opera and Edge on Windows 10, as well as Chrome and Firefox on Android. Other browsers are likely to work fine as long as they support WebAssembly or asm.js, and ES6.

Internet Explorer is explicitly incompatible due to lack of ES6 support. Additionally, Firefox 61 and lower requires the user to manually navigate to the generated ZIP blob because the blob won't download programatically for whatever reason. This is fixed in Firefox 62+.

## Features
### General
* Generate a perfectly formatted file structure in ZIP format, ready for direct extraction to your SD card. No additional setup necessary, just drag and drop!
* Save your setup so you can update everything later without reselecting all of the packages.

### Nintendo Switch
* Choose between a selection of common homebrew applications, tools and utilities, including:
	* Custom Firmwares (ex. SX OS, Atmosphere, ReiNX)
	* Homebrew Utilities (ex. Homebrew Menu, Checkpoint, JKSV, Tinfoil)
	* Emulators (ex. Salamander RetroNX, pSNES)
	* Games (ex. Mystery of Solarus DX, SDL Prince of Persia)
	* Fusee Payloads (ex. Hekate, BISKeyDump, BriccMii)
	* PC Utilities (ex. TegraRCMSmash)

## Usage
Head over to [https://www.sdsetup.com](https://www.sdsetup.com), select your console of choice, select the packages you want, and hit download! Once finished, simply **extract the contents of the sd folder** in the downloaded ZIP archive **to the root of your SD card!** Do what you wish with any additional folders included in the zip file.

## Issues
Please feel free [submit an issue](https://www.github.com/noahc3/sdsetup/issues) for any of the following reasons:
* A package is outdated
* A package's information is incorrect
* A package should be retrieved from a different/better source
* A browser other than Internet Explorer is incompatible
* Reporting a bug
* Suggesting a feature
* Suggesting a new package
* Requesting a package be removed Homebrew SD setup
* Reporting a redistribution clause license violation for a rehosted package
* Any other issue with the site or it's packages

## Build
Clone the repository and open the solution in Visual Studio. Build from there.

## Included Projects
* **SD Setup Blazor:** The web application itself, written in C# (and a little bit of JavaScript).
* **SD Setup Manifest Generator:** A GUI authoring tool for generating a valid manifest file with package information and where to retrieve files for download. It has some quirks, and not yet feature complete.

## Todo
* The project needs a lot of optimization. For example, converting things to components and setting up databinding on individual components to refresh only what UI needs to be refreshed rather than entire containers.

* I'd also like the project to drop pretty much all JavaScript interop, minus browser compatibility checks. Unfortunately, SharpZipLib, the only .Net Standard 2.0 compliant ZIP library I could find, has major problems in the virtualized browser environment, making JS interop necessary.

## Contributing
Feel free to make pull requests where you see fit!

## Credits
Please see https://www.sdsetup.com/credits for an up-to-date list of credits and sources for each package available.

Other credits:
* tomGER for working with me to keep this project up to date.
*   Steve Sanderson and contributors for making this great thing called  [Blazor](https://blazor.net/)
*   Rikumax25 / Jorgev259 for JSZip wrapper functions used in  [3SDSetup](https://github.com/jorgev259/3SDSetup)/[WiiuSetup](https://github.com/jorgev259/wiiusetup), ultimately making my life much easier
*   Chanan Braunstein for  [BlazorStrap](https://github.com/chanan/BlazorStrap)
*   Joonas W. for  [Using C# await against JS Promises in Blazor](https://joonasw.net/view/csharp-await-and-js-promises-in-blazor)

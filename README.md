<p align="center">
  <img height="200" src="https://i.imgur.com/laXau20.png">
</p>

## SketchCrapp

Sketch.App Patch Tool, brought to you by [@duraki](https://github.com/duraki) & [@elijahtsai](https://github.com/elijahtsai). This script provides you a quick and dirty way to patch Sketch.app for Unlimited Trial. You can always patch manually using Ghidra by following [this tutorial](https://duraki.github.io/posts/o/20200214-sketch.app-patch-in-ghidra.html). Offsets available [here](https://github.com/duraki/SketchCrapp/blob/master/README.md#offset-table).

**Download Sketch.App version of your choice here:** https://www.sketch.com/updates/

## Usage

* Open your MacOS Terminal (`Cmd+Space`, type **Terminal**)
* Type the commands below
* Download or clone this repository
  * `cd $HOME && git clone https://github.com/duraki/sketchcrapp`
* Make script executable
  * `cd $HOME/sketchcrapp && chmod +x sketchcrapp.sh`
* Run the script to patch Sketch.app
  * `cd $HOME/sketchcrapp && ./sketchcrapp.sh`

**Notice**→ The application should automatically detect your Sketch.App version. If not, you can pass `-a` argument for your Sketch.app Application Bundle.

```bash
crackb0x:SketchCrapp duraki$ ./sketchcrapp.sh -h
           __       __      __
      ___ / /_____ / /_____/ /  ___________ ____  ___
    ( _-</  '_/ -_) __/ __/ _ \/ __/ __/ _ `/ _ \/ _ \
    /___/_/\_\\__/\__/\__/_//_/\__/_/  \_,_/ .__/ .__/
                                          /_/  /_/
         Sketch.App Patch Tool (https://github.com/duraki/SketchCrapp)
         by @duraki & @elijahtsai

Usage:
./sketchcrapp [-h] [-a] <applicationPath> [-m]
Supported versions: v58, v63.1, v64.0, v65.1, v66.1, v67, v67.1, v67.2,
v68, v68.1, v68.2, v69, v69.1, v69.2
```

```
crackb0x:SketchCrapp duraki$ ./sketchcrapp.sh
           __       __      __
      ___ / /_____ / /_____/ /  ___________ ____  ___
    ( _-</  '_/ -_) __/ __/ _ \/ __/ __/ _ `/ _ \/ _ \
    /___/_/\_\\__/\__/\__/_//_/\__/_/  \_,_/ .__/ .__/
                                          /_/  /_/
         Sketch.App Patch Tool (https://github.com/duraki/SketchCrapp)
         by @duraki & @elijahtsai

[+] Analysing application bundle ... Starting
[+] Finding executable file ... OK
[+] Finding Info.plist ... OK
[+] Checking Info.plist for CFBundleShortVersionString ... OK
[+] Validating executable file ... OK
[+] Selected Sketch.app version is 69.2 ... SketchCrapp starting ... OK
[+] Patching offsets for 69.2 ... Starting
[+] Patching address at offset: 0x5d09df with value: \00
1+0 records in
1+0 records out
1 bytes transferred in 0.000026 secs (38480 bytes/sec)
[+] Patching address at offset: 0x5d09e2 with value: \00
1+0 records in
1+0 records out
1 bytes transferred in 0.000018 secs (55188 bytes/sec)
[+] Patching address at offset: 0x5cf57e with value: \00\00
2+0 records in
2+0 records out
2 bytes transferred in 0.000023 secs (87381 bytes/sec)
[+] Patching address at offset: 0x5cf6ae with value: \165
1+0 records in
1+0 records out
1 bytes transferred in 0.000018 secs (55924 bytes/sec)
[+] SketchCrapp certificate already exists.
[+] Skipping certificate creation ... OK
[+] Signing the patched *.app bundle. This may require root privilege.
[+] If asked, enter your login password. Choose "Always Allow" to not be asked again.
/Applications/Sketch.app: replacing existing signature
[+] Cleaning up file(s) ... Cleaned
[+] SketchCrapp process completed. Sketch.app has been patched :)
[+] -- Notice:
[+] If a dialogue shows up with message: “Sketch 3.app” can’t be opened
[+] please right-click the application and select open,
[+] or go to Settings -› Security and allow opening Sketch.app application.
[+]
[+] If you are using an old version and a dialogue shows up asking for password
[+] about "com.bohemiancoding.sketch3.HockeySDK"
[+] please enter your login password. Choose "Always Allow" to not be asked again.

[+] SketchCrapp (A Sketch.app cracking tool)
[+] https://github.com/duraki/SketchCrapp [by @duraki & @elijahtsai]
```

## Issues

If you have troubles using the script, please contact the team via GitHub Issues.

---
## Version Request

#### Higher Version

If the version you are trying to patch is higher than supported, please notify the team via GitHub Issues.

#### Lower Version

If you really need specific version you can contact the team via GitHub Issues, but we can only do our best to help you.


**Build with ❤️ by [@duraki](https://twitter.com/0xduraki) & [@elijahtsai](https://twitter.com/elijahtsai_)**

> [Original idea and thread](https://gist.github.com/Bhavdip/76c581d7ac03bdce6d226a2e8c522df4)

### Offset Table
|58|63.1|64|65.1|66.1|67 & 67.1|
|----|----|----|----|----|----|
|0x1003912c0|0x1004a2a50|0x1004cde70|0x1004db500|0x1004f3750|0x10050a6d0|
|0x10038ff14|0x1004a1724|0x1004ccb44|0x1004da1d4|0x1004f2424|0x100509394|
|0x10038ff2c|0x1004a1738|0x1004ccb58|0x1004da1e8|0x1004f2438|0x1005093a8|
|0x10038ff32|0x1004a173e|0x1004ccb5e|0x1004da1ee|0x1004f243e|0x1005093ae|
|0x10039007d|0x1004a1879|0x1004ccc99|0x1004da329|0x1004f2579|0x1005094e9|
|0x10039009a|0x1004a1896|0x1004cccb6|0x1004da346|0x1004f2596|0x100509506|

|67.2|68|68.1 & 68.2|69|69.1 & 69.2|
|----|----|----|----|----|
|0x10050a790|0x10054d2b0|0x10054d350|0x1005cf770|0x1005d09e0|
|0x100509454|0x10054bf74|0x10054c014|0x1005ce434|0x1005cf564|
|0x100509468|0x10054bf88|0x10054c028|0x1005ce448|0x1005cf57c|
|0x10050946e|0x10054bf8e|0x10054c02e|0x1005ce44e|0x1005cf582|
|0x1005095a9|0x10054c0c9|0x10054c169|0x1005ce589|0x1005cf6ae|
|0x1005095c6|0x10054c0e6|0x10054c186|0x1005ce5a6|0x1005cf6d2|

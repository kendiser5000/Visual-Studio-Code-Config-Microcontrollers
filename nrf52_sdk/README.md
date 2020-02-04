# Visual Studio Code Config NRF52x (v16 SDK)


In "c_cpp_properties.json":
- Change "nrfSDK" to path that contains sdk
- Change "compilerPath" to location of bin folder of arm gcc
- Add any defines to "defines"
- Add location of all source/header files

In "launch.json":
- Change "armToolchainPath" to location of bin folder of arm gcc
- Change "executable" to where build output would be (e.g. the .elf or .out)
- Change "servertype" to your debugger (e.g. jlink, stlink)
- Change "interface" to interface being used (e.g. swd, jtag)
- Change "device"

In "settings.json":
- Add files.association to go to definition of vars/constants

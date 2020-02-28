# Visual Studio Code Config

Config Files for Visual Studio Code (VS Code) using Cortex Debug

```javascript
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Cortex Debug",
            "cwd": "${workspaceRoot}",  
            "executable": "pca10056/blank/armgcc/_build/nrf52840_xxaa.out",     // location of your build file
            "request": "launch",                                                // Launch debugger
            "type": "cortex-debug",                                             // Select Debugger of Choice
            "servertype": "jlink",                                              // Select GDB server (jlink, stlink,)
            "device": "nrf52",                                                  // Indicate board model for debugger
            "interface": "swd",                                                 // jtag/swd
            "ipAddress": null,                                                  // if gdb server fill this
            "serialNumber": null,                                               // serial number of debugger
            "armToolchainPath": "/opt/gnuarmemb/bin/"                           // set toolchain path 
             //"preLaunchTask": "tasks",                                        // to add extra JSON with build commands
        }
    ]
}
```

Example "Launch.json" file for pretask
```javascript
{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "label": "tasks",
            "type": "shell",
            "command": "make",
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
} 
```

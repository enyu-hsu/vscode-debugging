# VS Code Debbugging Environment for Python
This is a guide to help you setup the VS Code debugging environment for Python locally and remotely, and is based on VS Code's documents on [debugging](https://code.visualstudio.com/docs/editor/debugging) and [Python debug configuration](https://code.visualstudio.com/docs/python/debugging).

## Install VS Code
You can download VS Code [here](https://code.visualstudio.com/).

## Setup Debugging Configuration for Python
Click on the debug icon in the sidebar.

![](images/debug_icon.png)

If you don't have any configuration yet, you will see "No Configurations". Click on the setting icon to create one.

![](images/no_configuration.png)

A configuration menu will then show up, choose **Python File**.

![](images/python_configuration.png)

This will create and open a `launch.json` file with default configuration located in a `.vscode` folder in your workspace (project root folder). You can modify or add custom configurations here. For more configuration options, checkout the [VS Code document](https://code.visualstudio.com/docs/python/debugging#_set-configuration-options).

<img src="images/launch_json.png" width="400" height="250">

## Launch versus Attach configuration
In VS Code, there are two ways to perform debugging actions, **Launch** and **Attach**. You may think of **launching** is to start your program in debug mode, and **attaching** is to attach the VS Code debugger to an **already** running process.

You may choose the way you prefer by setting the `"request"` argument to `"launch"` or `"attach"` in `launch.json`.

## Launching a Program in Debug Mode
With default configuration, you can launch a Python program locally in debug mode. Simply press `F5` to enter debug mode. The status bar below will turn orange and show the active launch configuration once you successfully enter debug mode.

![](images/debug_mode.png)

The debug toolbar will also show up for you to perform debug actions.

![](images/debug_toolbar.png)

#### Breakpoints
Breakpoints could be set by clicking on the **editor margin** or pressing `F9` on the current line. You may also call `breakpoint()` at any place in your Python code to pause the debugger.

![](images/breakpoint.png)

You can have more control of the breakpoints in Debug view's **BREAKPOINTS** section.

![](images/breakpoint_section.png)

For advanced breakpoints such as conditional breakpoints, inline breakpoints or function breakpoints, checkout [VS Code document](https://code.visualstudio.com/docs/editor/debugging#_advanced-breakpoint-topics).

#### Data Inspection
Variables can be inspected in the **VARIABLES** section, and variables can be modified with the **Set Value** action by right clicking on the variables. Note that the variable values are relative to the selected stack frame in the **CALL STACK** section.

![](images/variables.png)

You can also add variables or **expressions** to the **WATCH** section.

![](images/watch.png)

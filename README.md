# [ScottKirvan/ToolExample](https://github.com/ScottKirvan/ToolExample)
ToolExample contains UX/UI C/C++ examples for adding tools and UI elements to the [Unreal Engine](https://www.unrealengine.com) editor - which means, these are editor tools for the artist, and not an example of how to write the runtime game code that a player would interact with.  

If you're looking for an example to show how to add an item to the existing menu, or a new edit mode, or how to create a dockable window, this is a really thorough, [step-by-step example](https://lxjk.github.io/2019/10/01/How-to-Make-Tools-in-U-E.html) that starts from an empty code project, immediately jumps into the base modules needed, and then clearly walks through the steps to code up various UI elements, hooking them to functionality as you go.

# Features
These examples show how to implement the following:
- adding modules
- adding menus to the editor interface with:
  - sections
  - menu items
  - sub menus
  - adding custom widgets and controls (button and text input) to the menu
- adding a dockable tab Window
- custom details panel
- defining and adding your own custom asset data type (data factory)
- importing/reimporting custom data
- custom editor mode
- custom editor viewport widget
- viewport object context sensitive right-click & menus
- custom project settings/preferences
- additional tricks and tips

This repo is an updated fork of [Eric Zhang's](https://github.com/lxjk) original [UE4 project](https://github.com/lxjk/ToolExample).  The excellent step-by-step documentation can be found here: [How to Make Tools in UE4](https://lxjk.github.io/2019/10/01/How-to-Make-Tools-in-U-E.html)   I've included a stripped down version of that tutorial in this repo in case anything happens to that URL in the future.  

This tutorial has become the most valuable one I've run across in my Unreal C++ journey.  It got me started in an area of programming in Unreal that I found pretty impenetrable at first, and it has continued to be a reference point that I return to frequently whenever I'm thinking I want some new functionality (or just some easier-to-get-at functionality) inside Unreal.  My deepest gratitude to Eric for his contribution here.

## Branches
- master
    - current development branch - this will likely have the most recent code
- 5.1
	- UE 5.1 Compatible
	- There was some header changes, a new module dependency, and class FEditorStyle was deprecated and replaced with FAppStyle.
	- I tested this very briefly, but it all looks good!
- 4.26
  - UE 4.26 Compatible.
  - Example Editor Mode is working in this version, so I'm not going to bother trying to figure out what broke in 4.25.  If anyone takes this on as a project, please toss up a Pull Request.
  - initial branch source is identical to 4.24/4.25
- 4.25
    - UE 4.25 Compatible.
    - builds and runs, but the Example Editor Mode isn't working.  It shows up in the Modes list, but the UI never gets built when selected.  I didn't see any errors or warnings anywhere.
        - NOTE:  The editor mode issue works in 4.26 without any code changes.
    - as it stands, this source is identical to the 4.24 branch
- 4.24
    - UE 4.24 Compatible.
    - updates build.cs to V2 target.
        - implements [IWYU](https://docs.unrealengine.com/en-US/ProductionPipelines/BuildTools/UnrealBuildTool/IWYU/index.html) standard.
- 4.23
    - original fork from [lxjk/ToolExample](https://github.com/lxjk/ToolExample).
    - UE 4.23 compatible.

## Contributing
Do you know how to create a UI tool that would be good to include in this example?  Interested in contributing with writing or anything else?  Did you find a bug?! Please help out!   Check the issues link to see the kinds of things that might be fun to tackle.

The best way to contribute would be with Pull Requests (PR):  Fork this repository, make your changes, and submit a Pull Request that can be reviewed and rolled back in.

If you don't want to do the Write/PR process yourself, but would still like to contribute, just use the Issues link above to report bugs or request something new you'd like to see.  

## System Requirements
- Computer capable of Unreal Engine development
	- Epic Recommends: xxx
- Unreal Engine 5.1
	- This repo supports older versions, just clone the branch you need.
- Microsoft Visual Studio 2022
	- I believe the 2019 version works with UE5 also.

## Getting Started With Local Development
Clone or download this repo.  Double clicking the `uproject` file should launch Unreal, which will recognize it as a code project and build everything automatically.  

I highly recommend following the Tutorial and using this code as reference.  If you hit an error, look at this code to see what may have changed.


## Support
- 

## Submit a Feature Request
Use the [Issues](https://github.com/ScottKirvan/ToolExample/issues) link, above.

## Credits
Eric Zhang (2019)  
Scott Kirvan (2021-present)

*ToolExample is licensed under the [MIT License](LICENSE.md).*
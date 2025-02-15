# tawd-package

*This project is deprecated for use with Linux, which now makes use of Open Build Service to build multiple native Linux packages. This project is kept around for Windows installers, should anyone ever need them*

This is the release build module for **TAWD** and **Valkal's Shadow**, an upcomimg version of [Earth Eternal](https://www.theanubianwar.com). 

This build is the new server, re-purposed from it's original intention for an entirely new game storyline, to instead add lots of new features to the existing Earth Eternal game.

It provides :-  

  * NSIS installer for Windows
  * Debian package for Linux
  
3 Different packages will be produced for each target operating system.

  * tawd (the server itself, useless on it's own)
  * valkals-shadow-asset (contains client side assets, downloaded by the client boostrap)
  * valkals-shadow-data (contains server data, including scenery, quests, creatures etc)
  
All 3 most be installed for a complete working server.

## To Build

### Source Dependencies

You will need the following repositories cloned into the same parent directory as this one.
  
  * [sparkplayer-compiler](../sparkplayer-compiler) checked out (by default at ../sparkplayer-compiler from the root of this module)
  
  * [sparkplayer-eartheternal](../sparkplayer-eartheternal) (valkals_shadow_on_taw_server branch) checked out (by default at ../sparkplayer-eartheternal from the root of this module)
  
  * [tawd](../tawd) (iceee master branch) source checked out and compiled (by default at ../tawd from the root of this module) 

### 3rd Party Pre-requisites

The following tools are also needed to perform the build.
 
  * Java Runtime (for Ant and CAR compiler tools)
 
  * Ant
  
  * NSIS
  
  * Meson (tested with 0.50.0)
  
  * Ninja (tested with 1.8.2)
  
  * C++
  
Also see the [tawd/README.md](../tawd/README.md), [sparkplayer-eartheternal/README.md](../sparkplayer-eartheternal/README.md) and [sparkplayer-compiler/README.md](../sparkplayer-compiler/README.md) for other dependencies required to build the server.


### Procedure
 
  1. Run `ant release-windows` or `ant release-linux`
 
  1. Results will be in `target/release`

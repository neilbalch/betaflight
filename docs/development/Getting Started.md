# Getting Started with Contributing to Betaflight Development

## Intro

It is pretty common knowledge that the Betaflight repository was originaly a fork of [Cleanflight](github.com/cleanflight/cleanflight). There are still segments of the codebase that make references to the Cleanflight repository. :) Therefore, the basic file structure and coding style are incredibly similar to that of the Cleanflight repo.

Make references to [`docs/development/CodingStyle.md`](CodingStyle.md) and [`docs/development/Development.md`](Development.md) regarding coding style and philosophy respectively.
Make references to `docs/development/Building in [YOUR PLATFORM].md` for instructions on how to set up a workspace for Betaflight development

## Repository Structure

* `.[WHATEVER]/`: dotfile configurations for tools like GitHub and others
* `docs/`: Repository documentation separate from the Wiki
  * `API`: Docs describing the Betaflight MSP communication API
  * `boards`: Docs specific to individual FC boards
  * `CLI`: Docs on specific CLI commands
  * `development`: Intro to contributing to the repository
  * `Upgrading`: Tips for upgrading between Betaflight versions
  * `Wiring`: Tips for wiring individual FC boards
  * `[WHATEVER.md]`: Docs on specific functions of the codebase
* `downloads/`: Compressed downloads from `make` build system
* `lib/`: Fundimental libraries for common interaction with each supported processor
  * `main`: Drivers and middlewares for each supported processor
  * `test`: [GTEST](https://github.com/google/googletest) library that makes testing everything easier :)
* `make/`: Configuration files for `make`: *e.g. build flags list for each processor and instrucions per host OS*
  * `mcu`: Processor specific `make` configurations
  * `[WHATEVER.mk]`: General and host platform specific `make` configurations
* `obj/`: Built binaries from `make`, including flashable `.hex` files
  * `main`: Platform speicifc binaries
  * `test`: Test binaries (*one per unit test group*)
  * `[WHATEVER.hex]`: Flashable binaries for specific boards
* `src/`: Repository Source Code
  * `main`: Actual source for Betaflight runtime code
  * `test`: Source code for GTEST unit tests
  * `utils`
* `support/`: Various supportive libraries
* `tools/`: Linked libraries for the ARM platform
* Other: Various build scripts and markdown files
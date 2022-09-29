# Bela.pd

Library for working with [PureData](http://puredata.info) on the [Bela Platform](http://bela.io), enabling bidirectional communication between the same Pd patch running on Bela and a local machine. Half-live coding?

## Objects
- `bela.comms`: send and receive data to and from Bela
- `bela.send`: send data to Bela
- `bela.receive`: receive data from Bela
- `bela.name`: name an item of data to be sent to Bela
- `bela.scope`: easy access to the Bela oscilloscope

## Example
- **sliders** ([video](https://youtu.be/n1fM8_vGO88)). Send and receive data to and from Bela, with the same patch running on Bela and local machine.

![sliders](https://i.imgur.com/09SBCyW.png)

## Installation

- Download or clone this repository
- Create a Bela Pure Data project called `pd-externals`, see [this Wiki section for reference](https://github.com/BelaPlatform/Bela/wiki/Running-Puredata-patches-on-Bela#using-an-externals-folder)
- Copy the externals in `./bela.pd/pd-externals` to `pd-externals` to Bela, either by drag and drop via the IDE, or via the command-line:

```
scp /path/to/bela.pd/pd-externals/* root@bela.local:/root/Bela/projects/pd-externals
```
- Add `/path/to/bela.pd/pd-externals` to Pure Data's search path on your local machine

## Usage
- Add the `./bela.pd/render.cpp` to your Pure Data projects
- Run your project's `_main.pd` patch on Bela and your local machine at the same time
- See the example in `./bela.pd/examples/sliders` for more

## Todo/ideas

- Make `comms` work with non-static IP
- Saving and managing state and parameters
- A data logger on Bela
- Integration with other libraries like `ml.lib`
- Add more examples
- Rebuild `comms` using `send` and `receive`? Or, have `comms` sit in the background and a `bela.s` and `bela.r` per item of data.
- Add [CV-MIDI converters](https://github.com/BelaPlatform/Bela/tree/dev-modular/examples/08-PureData/midi-cv-midi)?
- `bela.scope~` compatibility with expander capelets

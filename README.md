# Bela.pd

Utilities for working with [PureData](http://puredata.info) on the [Bela Platform](http://bela.io)

## Objects
- `bela.comms`: send and receive data to and from Bela
- `bela.send`: send data to Bela
- `bela.receive`: receive data from Bela
- `bela.name`: name an item of data to be sent to Bela
- `bela.scope`: easy access to the Bela oscilloscope

## Installation

- Download or clone this repository
- Copy `pd-externals` to the folder `/root/Bela/projects/pd-externals` (create the folder first if needed - see [this GitHub issue](https://github.com/BelaPlatform/Bela/issues/384) for details)
- Copy to your local machine's PureData externals directory and add to PureData's search path
- Try an example patch
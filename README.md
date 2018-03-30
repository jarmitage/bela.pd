# Bela.pd

Library for working with [PureData](http://puredata.info) on the [Bela Platform](http://bela.io)

## Objects
- `bela.comms`: send and receive data to and from Bela
- `bela.send`: send data to Bela
- `bela.receive`: receive data from Bela
- `bela.name`: name an item of data to be sent to Bela
- `bela.scope`: easy access to the Bela oscilloscope

## Examples
- **sliders** ([video](https://youtu.be/n1fM8_vGO88)). Send and receive data to and from Bela, with the same patch running on Bela and local machine.

![sliders](https://i.imgur.com/09SBCyW.png)

## Installation

- Download or clone this repository
- Copy the custom libpd render to Bela ([in future](https://github.com/BelaPlatform/Bela/issues/390) use `Bela/examples/08-PureData/customRender`):

```
scp path/to/bela.pd/core/default_libpd_render.cpp root@192.168.7.2:/root/Bela/core/default_libpd_render.cpp
```

- Copy the pd-externals to Bela (create the folder on Bela first if needed - see [this GitHub issue](https://github.com/BelaPlatform/Bela/issues/384) for details):

```
scp /path/to/bela.pd/projects/pd-externals/* root@192.168.7.2:/root/Bela/projects/pd-externals
```

- Add `/path/to/bela.pd/pd-externals` to PureData's search path on your local machine
- Create a Pd project on Bela using e.g. the `/path/to/bela.pd/projects/sliders` example, and run the same patch locally 

## Todo/ideas

- Make `comms` work with non-static IP
- Saving and managing state and parameters
- A data logger on Bela
- Integration with other libraries like `ml.lib`
- Add more examples
- Rebuild `comms` using `send` and `receive`? Or, have `comms` sit in the background and a `bela.s` and `bela.r` per item of data.

# Gothic Texture Check CLI

Simple command line tool which checks folders for `.tga` or `.TEX` files and report if there are any missing animated or varied textures. :100: 

### Description

Gothic game textures require specific naming  in order to be loaded properly and work.

We have generaly three types:

* Animated
* Varied (Visual skin)
* Variend and Colored

The biggest concern here are the textures describing variations and color, such as `HUM_HEAD_V0_C0`.
In order to use texture `HUM_HEAD_V2_C1`, there must exist all the textures of lower order **(Variation up to 2 in every Color up to 1)**.

> `HUM_HEAD_V0_C0`
> `HUM_HEAD_V1_C0`
> `HUM_HEAD_V2_C0`
> `HUM_HEAD_V0_C1`
> `HUM_HEAD_V1_C1`
> `HUM_HEAD_V2_C1`
> etc.

### Features

* Find duplicates
* dicover missing texture variants
* discover missing animated texture frames

### Installation & Usage

Just extract .exe in your **Textures** folder and launch. This is default interactive mode of the application.

#### CLI
You can use the app with specified parameters to speed up the process.

```text
  Usage: GothicTextureCheck [options]

  Options:

    -h, --help             output usage information
    -v, --verbose          set app to verbose mode.
    -i, --interactive      the app will behave as with no parameters -> interactively asking what to do next.
    -d, --directory <path> path to the directory containing textures.
                           Usualy path to 'Gothic/_Work/Data/Textures'
                           or 'Gothic/_Work/Data/Textures/compiled/'
    -r, --recursive        recursively search all subfolders when looking for textures.
    --TGA                   include .tga extension when doing texture check.
    --TEX                   include .tex extension when doing texture check.
    -t, --tableStyle       change table style (Default, MarkDown, Alternative, Minimal).

    Examples:
        $ GothicTextureCheck -d <gothic root/_Work/Data/Textures> -r --TEX <= Check for missing or duplicated .TEX files.
        $ GothicTextureCheck -d <gothic root/_Work/Data/Textures> -r --TGA <= Check for missing or duplicated .TGA files.
        $ GothicTextureCheck -d <gothic root/_Work/Data/Textures> -i <= Run interactive check of textures
        $ GothicTextureCheck -d <gothic root/_Work/Data/Textures> -v -i <= Run interactive check with verbose input (more info)
```


**Download:**

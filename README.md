# Roboto Flex

This project upgrades Roboto to become a more powerful Variable Font, allowing you to do more to express and finesse your text.

**[Download latest development TTF](https://github.com/TypeNetwork/Roboto-Flex/raw/master/fonts/RobotoFlex%5Bslnt%2Cwdth%2Cwght%2Copsz%5D.ttf)**

## Background

_This project was commissioned by Google, but is not an official Google project, and Google provides no support for it._

Roboto became a flagship Google brand typeface in 2011, as the Android operating system UI type.
It is prominently positioned in the global design community, with Google using it on Android, in web apps, and for branded content at small sizes.
It is the default face of the Material Design Specification, and available to everyone under an unrestrictive license, it has been adopted by more than 11M websites and has become the most popular family in the Google Fonts library.

In 2016 the OpenType format was [updated](https://medium.com/@tiro/https-medium-com-tiro-introducing-opentype-variable-fonts-12ba6cd2369) with a revised version of Apple's “TrueType GX” run-time interpolation technology.
The primary motivation for the OpenType specification authors to do this was obtaining dramatic reductions in the file-size of large font families, such as Google's [Noto](https://github.com/googlei18n/noto-fonts/tree/master/phaseIII_only/unhinted/variable-ttf) fonts. 
The Google Fonts team intends to go beyond compression: They want to make variable fonts *meaningful*.

Variable fonts create a new dimension in typographic possibilities, and could improve Material Specification Typography guidance in myriad ways.
Today the Material typography guidelines include adjustments for tracking and font weight that are used to improve typographic-color and texture.
Variations allow those adjustments to be built-in and “just work.” 

After the public announcement of the technology, the Google Fonts team commissioned Font Bureau to develop a pilot project, [Amstelvar](https://github.com/TypeNetwork/Amstelvar), that demonstrates a novel approach that uses a system of inter-related axes. 
This increases the fine typographic control available to typographers, and enables a new kind of “parametric” typography.

Learn more about this new technology at [variablefonts.typenetwork.com](https://variablefonts.typenetwork.com)

## License

Fonts (UFO, TTF) are available under the [SIL Open Font License v1.1](OFL.txt)

Scripts and documentation are available under the [Apache 2.0](/scripts/LICENSE.txt)

## Source Files

**Do not edit fonts outside the `1-drawings` directory, they are intermediate build artifacts generated by the build script**

`1-drawings` contains the 'true' sources, in UFO format.

`build-roboto.py` then takes them and builds the variable font, outputting the instance UFOs in `master_ufo` and `instances` 

Those are build into TTFs using [fontmake](https://github.com/googlei18n/fontmake) which stores intermediate binaries in `master\_ttf\_interpolatable` and `master\_ttf`

These build intermediates are checked in to keep a full historical record, as they are used for debugging purposes.

The actual TTF you should use is in `/fonts`

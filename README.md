# Duotone to base16 colorscheme

> 1.0.0 - alpha

## Installation

```bash
git clone https://github.com/davidosomething/duotone-base16.git
cd duotone-base16
npm install
./db16
```

## Usage

```bash
./db16 <duotone-repo>
```

where `<duotone-repo>` is the github repo `username/themename` of an atom theme
in [duotone-syntax](https://github.com/simurai/duotone-syntax).

E.g.

```bash
./db16 simurai/duotone-dark-syntax
```

will generate the file `schemes/duotone-dark-syntax.yml`

Then you can compile that file using [base16-builder](https://github.com/chriskempson/base16-builder):

```bash
cp schemes/duotone-dark-syntax.yml $PATH_TO_BASE16_BUILDER/schemes
cd $PATH_TO_BASE16_BUILDER
./base16 -s schemes/duotone-dark-syntax.yml
```

This will generate various colorschemes, e.g. you can grab the VIM version from
`output/vim/duotone-dark-syntax.vim` and load that into VIM.

## Roadmap

- [x] CLI
- [x] Obtain duotone atom theme variants into temp dir
- [x] Compile via node [less module](https://www.npmjs.com/package/less) and convert HSL values to hex
- [x] Map to [base16 yaml scheme](https://github.com/chriskempson/base16-builder/tree/master/schemes)
    - [ ] HELP WANTED on mapping the colors to base16 colors, see `function convertToBase16(output)`


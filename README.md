# gadgets-vinci

Vinci for the gadgets of [polpo](https://github.com/polpo-system/polpo): a language for describing
graphics. A Vinci program is turned into Scheme (the package scheme) and run with operators for
drawing; it draws with Gfx on the screen, into EPS files (gfx-ps), or as shapes inside Leonardo
figures (gadgets-leonardo).

```
portia.Install gadgets-vinci
```

## Using

    VinciDocs.Open Smiley.Vinci        a Vinci program drawn in a document
    Desktops.OpenDoc Vinci.Text        the description of the language

The examples Clip, Labels, Smiley, Stars and Test (.Vinci), and five shapes for Leonardo (CoordSys,
Distance, NGon, Rect2, YinYang, .Shape) are in share/.

## What is here

    src/OLR.Vinci.Mod            the language
    src/VinciGadgets.Mod, VinciDocs.Mod             gadgets and documents
    src/VinciShapes.Mod, VinciPens.Mod, VinciEditors.Mod   Vinci shapes and pens in Leonardo
    share/Vinci.Init             the definitions read when Vinci starts
    share/Vinci.Text, *.Vinci, *.Shape
    tools/Vinci.Tool
    test/VinciTest.Mod

Vinci is by Erich Oswald. The sources come from ETH Linux Oberon (OLR, 2017-06-18), converted from Oberon texts to plain
text; the first commit has them unchanged. They compile unchanged with all five of polpo's compilers
(x86, ARM, ARMv7, RISC-V, MIPS).

## Tests

    VinciTest.Run      3 checks: a Vinci gadget made, Smiley.Vinci drawn in a document, a Vinci
                       shape made; it needs the desktop's display

The license is GPL-3 (`LICENSE`); the code comes from ETH Oberon, whose license (`LICENSE.ETH`)
asks to keep its copyright notice and conditions, which `LICENSE.ETH` does.

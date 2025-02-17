# TeensyPixel 2.0

![Board Image](/images/board_render.png)

TeensyPixel is a simple adaptor board designed to convert the Teensy 4.1's 3.3V logic level to the 5V required for WS2812B (NeoPixel) LED strips. It outputs the 5V PWM pins via 3 RJ45 ports, and exposes the rest of the unused Teensy pins for other uses. While it is designed for LED strips, it can likely be used for other 5V logic level devices as well.

## Files

The board was designed in EasyEDA Pro. The project file is located at [src_files/teensypixel.epro](/src_files/teensypixel.epro).

The schematic and PCB drawings are located in the [drawings](/drawings) folder.

The Gerber files are located in the [mfg_files](/mfg_files) folder.

## How to Order

While this board can be oredered from any PCB manufacturer, it is designed to be ordered from JLCPCB using components from LCSC. I stronly reccommend purchasing their assembly service as well if you're unafamaliar with soldering surface-mount components, this board has small parts not designed to be assembled by hand. Here are some brief instructions on the order process.

JLCPCB only allows ordering in increments of 5. Unfortunately there is no way around this, so you will have to order 5 boards at a time. The cost is still very reasonable, and you can always sell the extras to friends, or keep them as backups.

**Use common sense during the order process! I am not responsible for any mistakes you make, JLCPCB's processes may change over time. If you're confused on what an option means, Google is your friend.**

### Setting up the PCB

- Download the files in the [mfg_files](/mfg_files) folder.
- Visit [JLCPCB](https://jlcpcb.com) and click "Order Now" on their homepage.
- Drag the [gerber .zip file](/mfg_files/teensypixel_gerber.zip) into the upload box.
![Order Page](/images/order_page.png)
- You can leave the other options on the page on their default settings. If you want a different color, you can change it here. If you don't want lead in your board make sure to select the lead free HASL option under surface finish, this board doesn't require ENIG.
![Surface Finish](/images/surface_finish.png)
- Under PCB assembly, enable the toggle box. You can leave all the other settings here at their default option too.
![PCBA](/images/pcba.png)
- Click "Next" to continue

### Setting up Assembly

- In the upload fields, drag the [BOM file](/mfg_files/teensypixel_bom.csv) and [Pick and Place (CPL) file](/mfg_files/teensypixel_cpl.csv) into the respective boxes.
![BOM and CPL](/images/bom_cpl_upload.png)
- Click "Process BOM & CPL" to continue.
- There may be an error popup, saying something along the lines of M1 and CN2 not being found in the BOM file. This is normal, we don't want to assemble these components (these are the additional headers and the Teensy itself). Click continue.
- You will be taken to a page where you can review the components JLCPCB found in the BOM file. Make sure they match the components on the board. If they don't, you may have uploaded the wrong BOM file. Click "Next" to continue.
![Review Components](/images/bom_confirm.png)
- You will be taken to a page where you can review the component placements. It will generate a 3D model of the board, make sure the component placements are correct. Click "Next" to continue.
![Review Placements](/images/placement_confirm.png)

### Confirming the Order

- Finally, you will be taken to a full page with your final quote. If everything looks right, click "Save to Cart" to continue. You can then complete the order from your cart!

## License

TeensyPixel © 2025 by [Camdan Mead](https://camdan.me/) is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
![CC BY-SA 4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)

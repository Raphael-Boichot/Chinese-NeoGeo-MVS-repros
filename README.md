# Teardown of some Chinese NeoGeo MVS bootlegs / repros

## Disclaimer
- I do not own these bootleg cartridges, because piracy is bad, very very bad. Don't do this.
- Everything written here is for documentation only. You do whatever you want with it, not my concern.
- Any reuse of original content present here must be credited (in other word, cite the source / author).

## Summary
- Tests were made with sound going out from a [SmallCab deluxe V2 supergun](https://www.smallcab.net/supergun-deluxe-p-2166.html) equipped with a [dummy load](https://github.com/Raphael-Boichot/Neogeo-MVS-one-slot-stereo-mod#do-you-want-to-try-a-non-destructive-and-easy-mod-before-). This is clearly not the absolute way to experience the amazing sound quality of a NeoGeo MVS but the author has distinguished between sound glitches caused by his specific setup and those caused by the repro cartridges being tested, by comparing them with original games.
- Regular repros rely on rerouting (not exact copies) of genuine PCBs ([PROGBK1](https://wiki.neogeodev.org/index.php?title=PROGBK1), [PROGBK2](https://wiki.neogeodev.org/index.php?title=PROGBK2), [CHA512Y](https://wiki.neogeodev.org/index.php?title=CHA512Y), [PROG-EP](https://wiki.neogeodev.org/index.php/PROG-EP), [CHA32G](https://wiki.neogeodev.org/index.php/CHA42G), for example). They looks like official MVS releases from 2003 but are not (no matching with existing genuine cartridges). This is the only part always new in these cartridges. Quality is always super good (gold plating, slikscreen, solder masks, irreproachables).
- Shells can be new or refurbished. The new shells are harder to put together because the tolerances are a bit off with screws but they are still heavy and sturdy.
- Not a single chip on these board is brand new. 100% are recycled and present signs of prior use like left stickers, traces of old stickers, scratches, unreadable marking due to wear or sanding, etc. Most of them are obsolete and probably just e-waste but also frequently 5V / 5V tolerant !
- The 161-in-1 in "version 2" / black shell shown here looks [exactly like the 161 in 1 in "version 3"](https://wiki.neogeodev.org/index.php?title=161-in-1_Series_1), same design. My guess is that "version 3" / blue shell is now (2026) just a Chinese scam to pocket the added value of a potential ["all-in-one" or Vortex convert](https://github.com/xvortex/VTXCart) made by the buyer without taking any risk for the vendor who just sells stocks of a very particular "version 2", reshelled / restamped. Some are even stamped "all-in-one compatible" to confirm the scam. There is no small profit. The chronological evolutions of the 161-in-1 revisions follows exactly the [chronological discussions](https://www.neogeo-system.com/t7269-tuto-modification-mvs-cartouche-161in1-v2) on western forums about how to "improve it" (including the snake oil). [Reported glitches](https://wiki.neogeodev.org/index.php?title=161-in-1_Series_1) are ALWAYS the same. The said multicart is more or less [reverse-engineered](https://www.arcade-projects.com/threads/reverse-engineering-161-in-1-cartridge-to-change-rom-games.15069/) now.
- There is a mixture of 5V and 3.3V (5V tolerant) chips on these cartridges. Apart from the fact that this is half-ass job (there is plenty of room on the PCB to add serious bus transcievers for outgoing signals), the long term effect of this level mismatch is just inexistant for the MVS motherboard as even in the worst case scenario, 3.3V signals sent back to the MVS motherboard, it stays in the [tolerance margin of the 5V TTL chips of the NeoGeo](https://retrosix.wiki/wiki/digital-logic-levels). For the cartridges in the other hand, nothing to fear, they operate in their voltage tolerance range. In any case, voltage mismatch does probably not explain the glitches when present.
- Most games passing the Unibios 4.0 checksum with success work without major glitches. For the other ones, depends... There is probably a mix of botched hacks and issue with delay tolerances of the flash chips used. My guess is that some particular way of programming the NeoGeo sound chip (most of the glitches are sound artifacts) always induces bugs in the repros whatever the bootleg PCB configuration. Sound glitches go from barely noticeable to frankly irritating when you're used to play the genuine games.
- The value for money remains excellent for playing and spending quality time with friends. These are clearly not collectible items but they perfectly do the entertainment job for the price you can touch them in 2026 (around 60€ shippment included).
- As far as I understand / see on internet, all cartridges from different suppliers / vendors have the same glitches for a given game. They probably all originates from common ancestor bootlegs never updated because who cares apart from NeoGeo purists.

## Xenocrisis
- Test setup: MV1FZS recapped from fresh, beefy enough arcade power supply (5.00V during all tests), good quality sound amplifier after a High/Low impedance adapter.
- Supplier: [Kuqi - Vintage Arcade Store Store](https://www.aliexpress.com/store/1103076414), May 2026.
- Unibios 4.0 verdict: unknwon game (of course)
- Glitches: none after hours of playing.  Game itself is a good Smash TV clone for Genesis. Cartridge owner was expecting more "NeoGeo signature effects" like massive shrinking sprites. And Cthulhu as a random boss in a game that has nothing Lovecraftian, such a lack of taste!

**Sticker**
![](/Pictures/Xenocrisis_Sticker.JPG)

**PRG board top**
![](/Pictures/Xenocrisis_PRG_top.JPG)

Marking on the ALTERA MAX: EPM3256ATC144-10N ([ALTERA MAX 3000A family](/Datasheets/ALTERA_MAX_3000A.pdf)).

**PRG board bottom**
![](/Pictures/Xenocrisis_PRG_bottom.JPG)

**CHA board top**
![](/Pictures/Xenocrisis_CHA_top.JPG)

Marking on the ALTERA MAX (NEO 273): EPM7128STC100-15 ([ALTERA MAX 7000 family](/Datasheets/ALTERA_MAX_7000.pdf)).

**CHA board bottom**
![](/Pictures/Xenocrisis_CHA_bottom.JPG)

## King of the Monsters 2
- Test setup: MV1FZS recapped from fresh, beefy enough arcade power supply (5.00V during all tests), good quality sound amplifier after a High/Low impedance adapter.
- Supplier: [Vintage Video Game Family Accessories Store](https://www.aliexpress.com/store/1102921377), April 2026.
- Unibios 4.0 verdict: Checksum OK
- Glitches: none after hours of playing

**Sticker**
![](/Pictures/KOTM2_Sticker.JPG)

**PRG board top**
![](/Pictures/KOTM2_PRG_top.JPG)

Marking on the LATTICE (PCM): LC4128ZE ([ispMACH 4000ZE Family](/Datasheets/Lattice_4000ZE_family.pdf))

**PRG board bottom**
![](/Pictures/KOTM2_PRG_bottom.JPG)

**CHA board top**
![](/Pictures/KOTM2_CHA_top.JPG)

Marking on the ALTERA MAX (NEO 273): EPM7128STC100-7 ([ALTERA MAX 7000 family](/Datasheets/ALTERA_MAX_7000.pdf))

**CHA board bottom**
![](/Pictures/KOTM2_CHA_bottom.JPG)

## Sengoku 2
- Test setup: MV1FZS recapped from fresh, beefy enough arcade power supply (5.00V during all tests), good quality sound amplifier after a High/Low impedance adapter.
- Supplier: [Kuqi - Vintage Arcade Store Store](https://www.aliexpress.com/store/1103076414), January 2026.
- Unibios 4.0 verdict: Checksum OK
- Glitches: none after hours of playing

**Sticker**
![](/Pictures/Sengoku2_Sticker.JPG)

**PRG board top**
![](/Pictures/Sengoku2_PRG_top.JPG)

Marking on the LATTICE (PCM): LC4128ZE ([ispMACH 4000ZE Family](/Datasheets/Lattice_4000ZE_family.pdf))

**PRG board bottom**
![](/Pictures/Sengoku2_PRG_bottom.JPG)

**CHA board top**
![](/Pictures/Sengoku2_CHA_top.JPG)

Marking on the ALTERA MAX (NEO 273): EPM7128STC100-7 ([ALTERA MAX 7000 family](/Datasheets/ALTERA_MAX_7000.pdf))

**CHA board bottom**
![](/Pictures/Sengoku2_CHA_bottom.JPG)

## Metal Slug 5
- Test setup: MV1FZS recapped from fresh, beefy enough arcade power supply (5.00V during all tests), good quality sound amplifier after a High/Low impedance adapter.
- Supplier: [Guangzhou San Star Online Shop](https://www.aliexpress.com/store/202692), March 2026.
- Unibios 4.0 verdict: Checksum NG 
- Glitches: No graphical glitches - sound glitches like scratchy sound during some explosions, some oversaturated sound effects (similar to Metal Slug 4 on the 161 in 1)
- This board was clearly modified at some point (scratches, traces of desoldering)

**Sticker**
![](/Pictures/Metal_Slug5_Sticker.JPG)

**PRG board top**
![](/Pictures/Metal_Slug5_PRG_top.JPG)

Marking on the ALTERA MAX (PCM2): EPM3256ATC144-10N ([ALTERA MAX 3000A family](/Datasheets/ALTERA_MAX_3000A.pdf))

**PRG board bottom**
![](/Pictures/Metal_Slug5_PRG_bottom.JPG)

**CHA board top**
![](/Pictures/Metal_Slug5_CHA_top.JPG)

Marking on the ALTERA MAX (NEO 273): EPM7128STC100-7 ([ALTERA MAX 7000 family](/Datasheets/ALTERA_MAX_7000.pdf))

**CHA board bottom**
![](/Pictures/Metal_Slug5_CHA_bottom.JPG)

## Magician Lord
- Test setup: MV1FZS recapped from fresh, beefy enough arcade power supply (5.00V during all tests), good quality sound amplifier after a High/Low impedance adapter.
- Supplier: [Kuqi - Vintage Arcade Store Store](https://www.aliexpress.com/store/1103076414), May 2026.
- Unibios 4.0 verdict: Checksum OK 
- Glitches: No graphical glitches - sound glitches like saturated sound levels that jumpscares you (similar to Pulstar, end of level 4, in the 161-in-1). It is surprinsing for such an early game. Sounds glitches for this particular game are reported by several buyers on different Aliexpress stores, so they probably all share the same chip architecture / manufacturer.

**Sticker**
![](/Pictures/Magician_Lord_sticker.JPG)

**PRG board top**
![](/Pictures/Magician_Lord_PRG_top.JPG)

Marking on the ALTERA MAX (PCM): EPM7128STC100-6 ([ALTERA MAX 7000 family](/Datasheets/ALTERA_MAX_7000.pdf))

**PRG board bottom**
![](/Pictures/Magician_Lord_PRG_bottom.JPG)

**CHA board top**
![](/Pictures/Magician_Lord_CHA_top.JPG)

Marking on the ALTERA MAX (no marking on PCB): EPM7128STC100-6 ([ALTERA MAX 7000 family](/Datasheets/ALTERA_MAX_7000.pdf))

**CHA board bottom**
![](/Pictures/Magician_Lord_CHA_bottom.JPG)

## 161-in-1 "Series 2"
- Test setup: MV1FZS recapped from fresh, beefy enough arcade power supply (5.00V during all tests), good quality sound amplifier after a High/Low impedance adapter.
- Supplier: [Random Taobao supplier](https://www.taobao.com/), December 2025.
- Unibios 4.0 verdict: Checksum NG for all games, supports the Pick'n Mix
- Bugs: rare graphical glitches all documented - some sound glitches (also well documented). Overall, **always the same glitches whatever the alledged PCB revisions.** The cartridge tends to mess up the calendar and the book keeping in test mode (but not always), but it goes back to normal with a genuine cartridge. Very irritating with the factory MVS bios where it can trigger calendar errors and oblige you to play with the dip switches to erase backup ram. So the advice: **always use the 161-in-1 WITH the Unibios**.
- [list of games](/Datasheets/MVS_161_in_1_GL.pdf) (always the same, too many KOFs and crap hacks, not enough early games).

The owner of the cartridge (not me) has tried many "improvements" found on the internet to fix the sound issues (see next sections) without any success, so his conclusion: **"any fix to sound glitches of the 161 in 1 proposed on the internet is just bullshit or yet implemented in late revisions"**.

**Sticker**
![](/Pictures/161in1v2_sticker.JPG)

**PRG board top**
![](/Pictures/161in1v2_PRG_top.JPG)

CP1 and PCM2 are ([ALTERA MAX 3000](/Datasheets/ALTERA_MAX_3000A.pdf)) with marking EPM3256ATC144-10N. PCM2 is sanded for unknown reasons but the chip is the same as CP1 after some more investigation with grazing light.

The resistor ladders A103J, 9 pins (RP1, RP2, RP3) and the 470 µF electrolytic capacitors (instead of 100 µF from factory) were added by the cartridge owner post factory as (unsucessful) [attempt to fix sound glitches](https://www.neogeo-system.com/t7269-tuto-modification-mvs-cartouche-161in1-v2). This board also present signs of modifications to add or modify ceramic capacitors on [SDRMPX, SDPMPX, SDROE, SDPOE](https://www.neo-geo.com/forums/index.php?threads/pcm-sound-stability-fixes-multicarts-120-in-1-138-in-1-161-in-1-and-others.242857/) (22 to 47 pF), without making any difference.

U2 is a 8-bit [STC11F08XE](/Datasheets/STC11-10xx_Series_MCU.pdf) microcontroller. Function is unclear to me in the presence of 3 beefy ALTERA CPLDs.

Each board has its own voltage regulator (AMS1117) capable to produce 1A each at 3.3V, much enough to power the whole set of chips. The cartridge itself consumes about 500 mA (at 5V), versus about 250 mA (at 5V) for a regular MVS cartridge. Nothing that’s going to fry your MVS slot but a noticeable increase anyway. 

**PRG board bottom**
![](/Pictures/161in1v2_PRG_bottom.JPG)

The F0095H0 are [1 Gigabyte NOR Flash Memory](https://www.arcade-projects.com/threads/reverse-engineering-161-in-1-cartridge-to-change-rom-games.15069/page-4) chips with unusual, non-standard BGA/LGA package, so the small green sub-board/daughterboard (the green PCB you see underneath the black glue in the images) which is meant to adapt those custom pins to standard, edge-soldered pins. 4 chips = 4 Gigabytes but much room is lost due to rom alignement so the uncompressed fullset would not fit.

The yellow sticker indicates a chip refurbished from a pachinslot machine based on [Sabu to Ichi Torimonohikae](https://en.wikipedia.org/wiki/Sabu_to_Ichi_Torimono_Hikae) theme, containing "effects/cutscene data 2", from [NewGin Company](https://en.wikipedia.org/wiki/NewGin).

Some ceramic decoupling caps were missing, populated by 100 nF by the owner (educated guess about the correct value to use).

**CHA board top**
![](/Pictures/161in1v2_CHA_top.JPG)

The white sticker on the F0095H0 indicates a chip refurbished from a pachinslot based on [Seibu Keisatsu](https://en.wikipedia.org/wiki/Seibu_Keisatsu) theme, containing "effects/cutscene data 2", from [NewGin Company](https://en.wikipedia.org/wiki/NewGin). The show was popular in 2004, so the chip is probably about 20 years old.

U2 is another ([ALTERA MAX 3000](/Datasheets/ALTERA_MAX_3000A.pdf)) with marking EPM3256ATC144-10N.

**CHA board bottom**
![](/Pictures/161in1v2_CHA_bottom.JPG)

Some ceramic decoupling caps were also randomly missing, populated by 100 nF by the owner. Does not change anything.

Overall, this cartridge was more than OK for the $60 it was sold before the prices went crazy with the VERTEX mod. New customers: fly away, try TaoBao directly or wait for the next version, if any.

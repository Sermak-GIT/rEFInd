# Classroom theme for rEFInd

This is my first attempt at an eyecandy theme/skin for the [rEFInd](http://www.rodsbooks.com/refind/) boot manager.

Why?

1. Lack of interesting alternatives. There is 'minimal' and then there's just lazy and uninspired. If I'm going to bother having a graphical boot manager I want it to at least look nicer than generic icons over a flat or gradient background.

2. No other themes (that I'm aware of) support multiple resolutions natively. At a bare minimum I wanted something which looks equally good at both 1080p and 4K. As it stands this currently supports 1920x1080, 2560x1600, 3200x1800 and 3840x2400.

## Installation

This is not intended for people who don't have a good understanding of what they're doing or think they can just 'wing it'. If you don't at least have a reasonable understanding of how EFI boot loaders work, stick to following [the official rEFInd installation guide](http://www.rodsbooks.com/refind/installing.html) to get up and running with the stock theme and minimise the risk of getting yourself into trouble.

Futhermore, this is distributed as a mostly ready-to-go git repository for my own use. Outside of the theme files, tt only includes the EFI binary, drivers etc that interest me. If you need to do anything I don't such as run on a 32-bit system or access HFS+ partitions, this will not work for you. Again, follow the official rEFInd instructions to get up and running with the stock theme first.

**Continue at your own risk**

Assuming you have installed rEFId to your EFI partition under `/EFI/refind`:

1. Rename your original conf from `refind.conf` to something like `refind.bak.conf`

2. Copy `refind.conf`, `classroom_*.conf`, `fonts/` and `themes/` to `/EFI/refind`. 

If you want to run in 1920x1080 resolution with no manual boot entries, you're done. Otherwise:

3. Open `/EFI/refind/refind.conf` in a text editor. Follow the instructions within. Don't forget to
   change the icon paths if you're manually defining boot entries and using a resolution other than
   the default 1920x1080

## Limitations / bugs

* Fonts currently not implemented - but it's coming. I prefer a clean no-labels-etc look but fonts are coming.

* Incomplete redraw of scrolling arrows leave ugly rendering artefacts when scrolling back and forth - this is a rEFInd bug I intend to look into

* Not all OS logos implemented - I tried to cover most for popular and/or interesting options but some really don't interest me at all (e.g. OSX), others are just such ugly/lazy logos they don't deserve any effort (e.g. Slackware).

## Changelog

### vNext

* Font support
* Media type badges (HDD, USB, optical disc)
* Tools icons
* Simple labels (requires rEFInd patch)
* Better font support (requires rEFInd patch)
* Auto-detect icon support for more operating systems (requires rEFInd patch)

### v1.0

* Initial public release

## Credits / thanks

Thanks to Roderick W. Smith (rodsmith@rodsbooks.com) for keeping rEFIt alive and making it more usable than ever with rEFInd

Stock image credits:

* 	AGF81: https://www.deviantart.com/art/Wood-Planks-D632-329164545
* 	MattiaMc: https://mattiamc.deviantart.com/art/ChalkBoard-Texture-MC2015-506107812
* 	Yuyanda: https://yuyanda.deviantart.com/art/Chalk-on-Blackboard-texture-270362309
* 	n8bitgaming: https://www.reddit.com/r/BoJackHorseman/comments/6zw2ls/so_they_had_chalk_board_tables_at_the_ice_cream/
* 	Brian Koberlein: https://briankoberlein.com/2016/10/25/world-pure-imagination/

Operating system logos remain the property of their respective copyright owners and are adapted here under fair use provisions

## Support / contact

If you use an operating system which doesn't have a suitable icon included, feel free to get in touch. As long as someone is using it, I don't mind taking requests for additional icons.


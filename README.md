# Deus Ex Conky
I made this Conky config to match my DE-themed desktop. It’s small, lightweight and can be easily expanded or adjusted. A dark background is recommended.

![Screenshot showing Deus Ex Conky in action](screenshot.png?raw=true)

## Requirements
- The CPU temp display assumes lmsensors is installed and configured. Alternatively, adjust the config to use a different program.

## Installation
1. Clone or download the repository.
2. Copy the files from /src to your home directory.
3. Install required fonts: [FontAwesome](http://fontawesome.io) for icons and [Montserrat](https://fonts.google.com/specimen/Montserrat) for text.
3. (Optional) Open .conkyrc in your favourite editor and make adjustments as desired (see below).
4. Start conky.
5. …
6. Profit.

## Matching wallpapers
Here are a few to get you started: [Collection of DE:MD wallpapers](https://wall.alphacoders.com/by_sub_category.php?id=232039)

[The wallpaper I use with this config](https://wall.alphacoders.com/big.php?i=735551)

## Adjustments
### Available package updates
The configuration features an update counter using Pacaur. If you want to use pacman instead, have a different our helper or are not using an Arch-based distro, find the following snippet in .conkyrc and change it to fit your needs:
${execi 600 pacaur -Qu | wc -l}`

### Number of CPU cores
The default setup is for a CPU with four cores. For a different setup, remove or add individual CPU bars. They start with this line:
`${voffset 6}core 01 ${offset 18}${color B08A49}${cpubar cpu1 5,90}${alignr}${color}${cpu cpu1}%`

### Light background
Change `default_color = 'ffffff'` to a darker color.

`highlightColor = 'B08A49'` is the gold color used for bars, icons, and headlines. Replace with a darker shade of gold (if you like).

## Notes
Deus Ex is a registered trademark and belongs to Square Enix Ltd. I do not own any part of it.

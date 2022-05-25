# Leon's build of dwm
After 6 hour trying to get FiraCode work along side with a fallback font to display some cjk character which FiraCode does not support, with a font2 patch of my st, It seems that it is completely not working, only the first *char font* works, but font2 is not loading, all my Asian characters are blank in st.
I also tried alacritty, that indeed worked (cjk chars are displayed well), even I only set FiraCode in alacritty.yaml. I am quietly confussing about how these two behaviour different with each other when loading font.

STFW for about 4 hours still brings me no luck, so finally I yield 😥

In dwm(config.h), I bind MOD+Return to use [FiraCode](https://github.com/tonsky/FiraCode/) `st -f FiraCode:size=16` and Shift+Return to use [Hack](https://github.com/source-foundry/Hack) font.
That totally not cool, but... anyway did work...

## Patches and features

- [Clickable statusbar](https://dwm.suckless.org/patches/statuscmd/) with my build of [dwmblocks](https://github.com/lukesmithxyz/dwmblocks).
- Reads [xresources](https://dwm.suckless.org/patches/xresources/) colors/variables (i.e. works with `pywal`, etc.).
- scratchpad: Accessible with mod+shift+enter.
- New layouts: bstack, fibonacci, deck, centered master and more. All bound to keys `super+(shift+)t/y/u/i`.
- True fullscreen (`super+f`) and prevents focus shifting.
- Windows can be made sticky (`super+s`).
- [stacker](https://dwm.suckless.org/patches/stacker/): Move windows up the stack manually (`super-K/J`).
- [shiftview](https://dwm.suckless.org/patches/nextprev/): Cycle through tags (`super+g/;`).
- [vanitygaps](https://dwm.suckless.org/patches/vanitygaps/): Gaps allowed across all layouts.
- [swallow patch](https://dwm.suckless.org/patches/swallow/): if a program run from a terminal would make it inoperable, it temporarily takes its place to save space.



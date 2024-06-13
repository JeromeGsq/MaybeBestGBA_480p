Edit from Kot4san: Thank you very much for your work mugwomp93. For "_maybe_best_gba_480p" you may not follow the next lines.

Perfect GBA Overlays for the RG35XX

**DO NOT USE THESE OVERLAYS WITH THE MIYOO MINI (PLUS)**

These files are adapted for the RG35XX from u/1playerinsertcoin's Perfect GBA overlay for the Miyoo Mini Plus (https://www.reddit.com/r/MiyooMini/comments/18ovuld/i_made_a_game_boy_advance_overlay/?rdt=52022). All credit goes to them - my only contributions are minor fixes and the borders on the _mugwomp93 overlays. 

Due to differences in the video output of the Miyoo Mini Plus and the RG35XX, the bottom border needed to be three pixels taller to properly align with the RG35XX GBA output (i.e., 424p instead of 427p). Please refer to the original post for files and settings for the MM+.

Note that these overlays have been tested on the original RG35XX with Garlic 1.4.9. I have no idea how they look on the Plus, H, or with different firmware.

******

Thank you very much to 1playerinsertcoin for generating proper 424p grids specifically for the RG35XX! Using the original grid for the MM+ introduced a few annoying (albeit minor) artifacts that are not present using the new grid.

The zip includes both the optimized and bright (brt) versions of the Perfect GBA grid. The grid of the bright version isn't quite as dark as the optimized version, though this comes at the expense of accuracy. If you find the bright version is still too dark, you could customize the overlay by adjusting the opacity of one of the _noframe variants and then applying your preferred version of the _nogrid (i.e., borders and dropshadow only) variants over top in Photoshop, GIMP, etc. Again, this comes at the expense of accuracy.

There are few minor interpolation artifacts that are visible using the new grid. These artifacts are present even without the overlay and appear as mid-tone bands or shadows on well-defined object borders (the question blocks in World 1-1 of Super Mario Advance 4 are really good for seeing this - some (but not all) have light gray borders on their top and/or bottom edges). The Perfect GBA grid actually hides or minimizes many of these, just not all. These artifacts are likely due to differences between Bilinear4X and Bicubic interpolation (which is recommended for the MM+ and not available in Garlic 1.4.9). The bright (brt) versions are less effective at hiding these artifacts as the grid isn't quite as dark.

The recommended Retroarch settings (adapted from the first comment on the Reddit post) are:

1. Core Options:

    Video > Color Correction > OFF

    Video > Interframe Blending > Simple (NOTE: If you don't like the image ghosting, turn it OFF, but you may see flickering elements in games.)


2. Video Settings:

    Integer Scale OFF

    Keep Aspect Ratio ON

    Image Interpolation > Bilinear4X (RG35XX does not have Bicubic interpolation)

    Video Filter > Normal4X.filt (GBA > Filter for overlays > GBAOffset.filt does not work on the RG35XX)


There's a lot of interesting discussion in the comments of the Reddit post - I highly recommend reading through them if you're interested in the technical details and process that were used to create these overlays.

-mugwomp93
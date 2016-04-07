# autotile

An auto-tiling script built for Game Maker Studio. This script will choose the correct image to display on a given tile based on the tiles around it. The script uses an efficient binary numbering system to quickly determine which image to show. The script requires that the tiles of your sprite are in a specific order, but this order is based on a binary counting pattern.

Once given a sprite with the necessary images, this script can be run as follows in the creation event for your wall object:

    image_speed = 0;
    scr_autotile(self);

If "X" is your block, then let the block spaces on the edges around your block be given values clockwise starting from the top as follows:

       | 1 | 
    ---+---+---
     8 | X | 2
    ---+---+---
       | 4 |
       
Now add the numbers of the blocks that are present on those edges together to get a unique number representing the configuration of blocks on the edges of your block, X. There are 16 ways the blocks can be configured on the top, bottom, left, and right of your block.

Now let the corners be numbered similarly.

     1 |   | 2
    ---+---+---
       | X |
    ---+---+---
     8 |   | 4
     
This time, rather than simply adding the numbers of present blocks together, we also determine if a corner has both edges surrounding it before adding it to our corner total. If a corner is not surrounded by both edge blocks, its presence has no effect on the appearance of block X.

There are 47 unique configurations around your block X that will affect its appearance. The correct image can now be decided via a 2-deep, nested switch statement:

    // edges   = total from present edge blocks
    // corners = total from present corner blocks surrounded by edge blocks
    
    switch(edges)
    {
        case 0: image_index = 0; break;
        case 1: image_index = 1; break;
        case 2: image_index = 2; break;
        case 3:
            switch(corners)
            {
                case 0: image_index = 3; break;
                case 2: image_index = 4; break;
            }
        break;
        case 4: image_index = 5; break;
        case 5: image_index = 6; break;
        case 6:
            switch(corners)
            {
                case 0: image_index = 7; break;
                case 4: image_index = 8; break;
            }
        break;
        case 7:
            switch(corners)
            {
                case 0: image_index = 9; break;
                case 2: image_index = 10; break;
                case 4: image_index = 11; break;
                case 6: image_index = 12; break;
            }
        break;
        case 8: image_index = 13; break;
        case 9:
            switch(corners)
            {
                case 0: image_index = 14; break;
                case 1: image_index = 15; break;
            }
        break;
        case 10: image_index = 16; break;
        case 11:
            switch(corners)
            {
                case 0: image_index = 17; break;
                case 1: image_index = 18; break;
                case 2: image_index = 19; break;
                case 3: image_index = 20; break;
            }
        break;
        case 12:
            switch(corners)
            {
                case 0: image_index = 21; break;
                case 8: image_index = 22; break;
            }
        break;
        case 13:
            switch(corners)
            {
                case 0: image_index = 23; break;
                case 1: image_index = 24; break;
                case 8: image_index = 25; break;
                case 9: image_index = 26; break;
            }
        break;
        case 14:
            switch(corners)
            {
                case 0: image_index = 27; break;
                case 4: image_index = 28; break;
                case 8: image_index = 29; break;
                case 12: image_index = 30; break;
            }
        break;
        case 15:
            switch(corners)
            {
                case 0: image_index = 31; break;
                case 1: image_index = 32; break;
                case 2: image_index = 33; break;
                case 3: image_index = 34; break;
                case 4: image_index = 35; break;
                case 5: image_index = 36; break;
                case 6: image_index = 37; break;
                case 7: image_index = 38; break;
                case 8: image_index = 39; break;
                case 9: image_index = 40; break;
                case 10: image_index = 41; break;
                case 11: image_index = 42; break;
                case 12: image_index = 43; break;
                case 13: image_index = 44; break;
                case 14: image_index = 45; break;
                case 15: image_index = 46; break;
            }
        break;
    }

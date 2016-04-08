#Tile Guide
This guide is just a reference for the order in which the tiles should exist to be referenced correctly by the autotile script.

The order is a pattern, but just in case, he's the definitive guide.

    // 'X' - block we're autotiling
    // 'B' - a space that must have a block in it
    // ' ' - a space that must be empty
    // '`' - A space that can be empty or full; doesn't matter
    
     tile 0     tile 1     tile 2     tile 3     tile 4     tile 5     tile 6     tile 7
    [`][ ][`]  [`][B][`]  [`][ ][`]  [`][B][ ]  [`][B][B]  [`][ ][`]  [`][B][`]  [`][ ][`]
    [ ][X][ ]  [ ][X][ ]  [ ][X][B]  [ ][X][B]  [ ][X][B]  [ ][X][ ]  [ ][X][ ]  [ ][X][B]
    [`][ ][`]  [`][ ][`]  [`][ ][`]  [`][ ][`]  [`][ ][`]  [`][B][`]  [`][B][`]  [`][B][ ]
    
     tile 8     tile 9     tile 10    tile 11    tile 12    tile 13    tile 14    tile 15
    [`][ ][`]  [`][B][ ]  [`][B][B]  [`][B][ ]  [`][B][B]  [`][ ][`]  [ ][B][`]  [B][B][`]
    [ ][X][B]  [ ][X][B]  [ ][X][B]  [ ][X][B]  [ ][X][B]  [B][X][ ]  [B][X][ ]  [B][X][ ]
    [`][B][B]  [`][B][ ]  [`][B][ ]  [`][B][B]  [`][B][B]  [`][ ][`]  [`][ ][`]  [`][ ][`]
    
     tile 16    tile 17    tile 18    tile 19    tile 20    tile 21    tile 22    tile 23
    [`][ ][`]  [ ][B][ ]  [B][B][ ]  [ ][B][B]  [B][B][B]  [`][ ][`]  [`][ ][`]  [ ][B][`]
    [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][ ]  [B][X][ ]  [B][X][ ]
    [`][ ][`]  [`][ ][`]  [`][ ][`]  [`][ ][`]  [`][ ][`]  [ ][B][`]  [B][B][`]  [ ][B][`]
    
     tile 24    tile 25    tile 26    tile 27    tile 28    tile 29    tile 30    tile 31
    [B][B][`]  [ ][B][`]  [B][B][`]  [`][ ][`]  [`][ ][`]  [`][ ][`]  [`][ ][`]  [ ][B][ ]
    [B][X][ ]  [B][X][ ]  [B][X][ ]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]
    [ ][B][`]  [B][B][`]  [B][B][`]  [ ][B][ ]  [ ][B][B]  [B][B][ ]  [B][B][B]  [ ][B][ ]
    
     tile 32    tile 33    tile 34    tile 35    tile 36    tile 37    tile 38    tile 39
    [B][B][ ]  [ ][B][B]  [B][B][B]  [ ][B][ ]  [B][B][ ]  [ ][B][B]  [B][B][B]  [ ][B][ ]
    [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]
    [ ][B][ ]  [ ][B][ ]  [ ][B][ ]  [ ][B][B]  [ ][B][B]  [ ][B][B]  [ ][B][B]  [B][B][ ]
    
     tile 40    tile 41    tile 42    tile 43    tile 44    tile 45    tile 46   
    [B][B][ ]  [ ][B][B]  [B][B][B]  [ ][B][ ]  [B][B][ ]  [ ][B][B]  [B][B][B]  
    [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  [B][X][B]  
    [B][B][ ]  [B][B][ ]  [B][B][ ]  [B][B][B]  [B][B][B]  [B][B][B]  [B][B][B]

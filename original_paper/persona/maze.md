# **1. Summary**  
- **tiles** Is a list saved a tile which contains the event, the width, height, etc.

# **2. FAQ**  
1. def turn_coordinate_to_tile
   - A method turns the coordinate from pixel into tiles(logical unit)
   - Conversion from pixel to tile coordinates simplifies interactions by translating physical positions into discrete logical locations.
2. self.address_tiles
   - The self.address_tiles dictionary maps addresses (like sector, arena, or game_object) to the set of all tiles associated with that address.
   - Example:  
     - Suppose the maze contains:  
       A kitchen (arena) spanning tiles (10, 5), (10, 6), (11, 5), and (11, 6).  
       A bed (game_object) located at (12, 7).
     - Output:
       ```
       self.address_tiles = {"double studio:kitchen": {(10, 5), (10, 6), (11, 5), (11, 6)},
       "double studio:kitchen:bed": {(12, 7)},}
       ```
3. In access_tile, why is the tile indexed as x, y, but in self.tiles, it is y, x?  
   - (x, y) aligns with traditional Cartesian coordinates.
   - [y][x] aligns with how 2D arrays are typically indexed in programming (row-major order).  









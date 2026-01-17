# MinecraftCOT — Build and Distribution Guide

## For other users (no development environment)

### Prerequisites
- Minecraft Java Edition with Fabric Loader installed
- Existing Minecraft world or server

### How to install and use

1. **Get the mod**
   - Download `MinecraftCOT-1.0.X.jar` from the distribution
   - This is the complete, compiled mod ready to use

2. **Install the mod**
   - **Single-player**: Copy `MinecraftCOT-1.0.6.jar` into:
     ```
     <your-minecraft-folder>/mods/
     ```
   - **Server**: Copy `MinecraftCOT-1.0.6.jar` into:
     ```
     <your-server-folder>/mods/
     ```

3. **Start Minecraft**
   - Launch the game with Fabric Loader 
      - fabric-loader-0.18.4
      - Minecraft-1.21.11
   - Load your world or start a new one
   - The mod will automatically begin exporting GeoTIFF files

4. **Find your maps**
   - GeoTIFF files appear in your Downloads folder:
     - `<world-name>.tif` - Visual map (RGB)
     - `<world-name>_elev.tif` - Elevation data (DEM)
   - Files update automatically as you explore

5. **Use in TAKX**
   - Load `<world-name>.tif` as a visual layer
   - Load `<world-name>_elev.tif` as elevation source
   - Player positions stream via UDP (default: 127.0.0.1:4242)

6. **Configure CoT (optional)**
   Add these JVM arguments when launching Minecraft:
   ```
   -Dminecraftcot.cot.host=255.255.255.255
   -Dminecraftcot.cot.port=4242
   -Dminecraftcot.cot.rateHz=2
   ```

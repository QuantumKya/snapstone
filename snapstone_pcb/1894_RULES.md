# Organization

## Project Hierarchy

1. Each distinct redstone part gets its own subfolder in `snapstone\_pcb`, which houses its KiCad project. Make a new subfolder when creating a new part.
2. Symbols made for the project are stored in the `snapstone.kicad\_sym` library.
3. When importing files for a new device/module/etc., put them in a dedicated subfolder of the `part\_files` folder, in this configuration:
```
part\_files/
├── NEW\_PART\_X/
     ├── NEW\_PART\_X.pretty/
     └── NEW\_PART\_X.kicad\_sym
```





# Practices

## Symbol Standards

**3\_Pin\_Block\_Connector**:

- Name symbol C\_IN or C\_OUT depending on its purpose in the schematic; e.g., a redstone repeater would have C\_IN1, C\_OUT1
- Use global labels `VCC` and `GND` to connect to the VCC and GND ports of the connector, NOT the default power symbols.
- Label distinctly the `VCC` and `GND` labels if they come from different C\_IN connectors; e.g., C\_IN1 => `VCC1`, C\_IN2 => `VCC2`, `VCC1` => C\_OUT1

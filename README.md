# klipper_config_v2_464
Voron 2.464 klipper config backup

- Used Cmponent  
   - Galileo Z Drive  
   - Bontech LGX
   - 
- SuperSlicer 2.4  

>Printer Custom G-Code 
  
    [Start G-code]  
    M104 S0 ; Stops PS/SS from sending temp waits separately
    M140 S0
    PRINT_START BED=[first_layer_bed_temperature] EXTRUDER={first_layer_temperature[initial_extruder]+extruder_temperature_offset[initial_extruder]} MATERIAL=[filament_type] CHAMBER=[chamber_temperature] SIZE={first_layer_print_min[0]}_{first_layer_print_min[1]}_{first_layer_print_max[0]}_{first_layer_print_max[1]}
    _ERCF_CHANGE_TOOL_STANDALONE  TOOL={initial_extruder}
    CLEANNOZZLE  
            
    [End G-code]  
    PRINT_END  
            
    [Tool Change G-code]  
    T[next_extruder]  
            
    [Coulor Change G-code]  
    M600  
               
    [Pause Print G-code]  
    PAUSE  
  
  >Filament Custom G-Code 
  
    [Start G-code]  
    SET_PRESSURE_ADVANCE ADVANCE=0.055


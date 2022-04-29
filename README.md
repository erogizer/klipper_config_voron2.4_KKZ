# klipper_config_v2_464
Voron 2.464 klipper config backup

- SuperSlicer 2.4  

  Printer Custom G-Code 
  
    1.Start G-code  
            M104 S0 ; Stops PS/SS from sending temp waits separately
            M140 S0
            PRINT_START BED=[first_layer_bed_temperature] EXTRUDER={first_layer_temperature[initial_extruder]+extruder_temperature_offset[initial_extruder]} MATERIAL=[filament_type] CHAMBER=[chamber_temperature] SIZE={first_layer_print_min[0]}_{first_layer_print_min[1]}_{first_layer_print_max[0]}_{first_layer_print_max[1]}
            _ERCF_CHANGE_TOOL_STANDALONE  TOOL={initial_extruder}
            CLEANNOZZLE  
            
    2.End G-code  
            PRINT_END  
            
    3.Tool Change G-code  
            T[next_extruder]  
            
    4.Coulor Change G-code  
            M600  
            
    5. Pause Print G-code  
            PAUSE  



Created by Gabriel Fornari on 19/06/2018
Last update on 02/10/2018


New changes
   - Stabilized version for using with battery
     -> "prints' removed
   - Pressure measurement fixed 
     -> Temperature measurements caused problems to the pressure measurement
     
   # Some issues   
     # DHT is giving 1º higher and 1% higher then normal
     # MPU temperature is wrong
     # MPU acce and gyro should be improved

     # Turn out the leds to save energy (not working)
     # Too much time is wasted to save data in File
       # It can be reduced if File open() and close() are removed
       # Maybe if I add flush()...
       # If File open()/close() are removed, the time to measure should be rearranged
     # Vin voltage should be measured
     # Saving data into File sometimes takes 200 ms (don't know why)
     # Change millis() to reset it every new second

Old Changes

 v2.3
   - MPU6050 measurements are saved in File
   - BMP180 measurement time is now reduced (parallelized)
   - DHT22 measurement time is reduced (time reduced)
   - BH1750 resolution changed to low_mode
   - Overall measurement time reduced to ~13 ms
   - File saving takes about ~36 ms

 v2.2
   - BH1750 is now working with different measurement time (MTreg = 32)
     - Minimum sample rate of BH1750 should be ~65 ms
   - Time (subsecond) was improved
   
 v2.1
   - Sample ratio is changing when the time (second) changes
   - BH1750 has overflow if value is bigger then 32755
   - Gyro should have raw values (instead of values converted to euler angles)

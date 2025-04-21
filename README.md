# STORMS
further research on wind data 

# Input Data
Input data (IBTrACS) is obtained and preprocessed from 
https://www.ncei.noaa.gov/products/international-best-track-archive

Preprocessing steps include:
1. Unify the reported wind speeds to 10-minute average sustained wind speeds (U10; in m/s) (due to differences in reporting methods), multiply by a factor of 0.88 to convert them to U10.
2. Extract storms from modern satellite era (post 1980)
3. For each basin (we can focus on North Atlantic), we extract the storms at all consecutive time steps where the U10 is greater than 18 m/s, or where the TC has not reached an extratropical cyclone-classification in the IBTrACS dataset (to ensure storms are TCs).
4. Linearly interpolate all extracted data to 3-hourly values
5. MSLP & SST data needed (they use ERA-5 from ECMWF for this).

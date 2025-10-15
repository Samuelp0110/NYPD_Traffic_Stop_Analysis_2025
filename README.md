### Database Tables
The reason for two different tables lies in the fact that the native data downloaded from the datasource is not separated by type and has questionable values

#### Vehicle_Stop_Data_Raw
CREATE TABLE vehicle_stop_reports_raw (
    evnt_key TEXT,
    occur_dt TEXT,
    occur_tm TEXT,
    cmd_cd TEXT,
    veh_seized_flg TEXT,
    veh_searched_flg TEXT,
    veh_search_consent_flg TEXT,
    veh_checkpoint_flg TEXT,
    force_used_flg TEXT,
    arrest_made_flg TEXT,
    summon_issued_flg TEXT,
    veh_category TEXT,
    rpted_age TEXT,
    sex_cd TEXT,
    race_desc TEXT,
    latitude TEXT,
    longitude TEXT,
    x_coord_cd TEXT,
    y_coord_cd TEXT
);

#### NYPD_Vehicle_Stop_Data
CREATE TABLE nypd_vehicle_stop_reports (
    event_key VARCHAR,
    date_occurred DATE,
    time_occurred TIME,
    command_code VARCHAR,
    vehicle_seized BOOLEAN,
    vehicle_searched BOOLEAN,
    vehicle_search_consent BOOLEAN,
    vehicle_checkpoint BOOLEAN,
    force_used BOOLEAN,
    arrest_made BOOLEAN,
    summons_issued BOOLEAN,
    vehicle_category VARCHAR,
    reported_age INT,
    sex_code VARCHAR,
    race_description VARCHAR,
    latitude FLOAT8,
    longitude FLOAT8,
    x_coordinate NUMERIC,
    y_coordinate NUMERIC
);

## Random Thoughts
- Modeling done after multiple attempts, understanding that predictions are impossible in this situation, whether with only contextual info or results of the stop

Emphasizes how important training officers are, as a stop, presumably similar to all situations, is a random event. An officers decisions in the moment are a 'black boix' of sorts, and they need to be capable to ensure its contents are proper. 

Article guide

Intro
data visualizations
interpretation
models
conclusion
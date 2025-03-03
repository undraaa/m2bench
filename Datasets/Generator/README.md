## How to generate Ecommerce datasets
M2bench Ecommerce datasets are generated based on TPC-DS and Unibench datasets.
Please download TPC\_DS datasets (SF=1) and Unibench dataset (SF=1).

*Requirements
    python packages: "pip3 install randomtimestamp"
                     "pip3 install pandas"

*Usage
    Run "python3 Ecommerce/main.py [arg1] [arg2]"
    (arg1: directory_path_to_tpcds_datasets,  arg2: directory_path_to_Unibench_datasets)

    ex) python3 main.py /home/user/Documents/tpc-ds-3.0.1/v3.1.0rc2/datas/ /home/user/Documents/Unibench_sf1/


## How to generate Healthcare datasets 

Step1. Please download following datasets.

1. MIMIC II Clinical Dataset
2. SNOMED Terminology
3. Drugbank (drug json data)

Step2. Run python3 Healthcare/main.py [arg1][arg2][arg3][arg4]
        (arg1: directory path to drugrugbank json dataset
        arg2: file path to SNOMED Concept description file from Snapshot library (e.g: Snapshot/Terminology/ Description_Snapshot.txt) 
        arg3: file path to SNOMED Concept relationship file from Snapshot library (e.g: Snapshot/Terminology/ Relationship_Snapshot.txt) 
        arg4: directory path to MIMIC II dataset* )
        
* Caution:  Do not forget to extract the files in the MIMIC II dataset directory before usage. 
            Make sure the dataset directory names does not contain characters such as : "()". 
            Keep in mind that arg1, arg4 are directory paths and arg2, arg3 are file paths.
         
* Requirements:  
    python pandas package: "pip3 install pandas"
    python names package: "pip3 install names"
    python glob package: "pip3 install glob3"


## How to generate Disater datasets 

* Data Source
    1.Earthquake: United States Geological Survey (USGS)
    (https://earthquake.usgs.gov/earthquakes/search)

    2.Shelter: Homeland Infrastructure Foundation-Level Data (HIFLD)
    (https://hifld-geoplatform.opendata.arcgis.com/datasets/national-shelter-system-facilities)

    3.Road Network: 9th DIMACS Implementation Challenge - Shortest Paths
    (http://www.diag.uniroma1.it//~challenge9/download.shtml)

    4.GPS: SEDAC Gridded Population of the World (GPW), v4
    (https://sedac.ciesin.columbia.edu/data/set/gpw-v4-admin-unit-center-points-population-estimates-rev11/data-download)

    5.OSM: Open Street Map (https://download.geofabrik.de/)

    6.Finedust: MISE, An Array-Based Integrated System for Atmospheric Scanning LiDAR (SSDBM 2021)

* Usage
    Run "python Disaster/main.py [arg1] [arg2] [arg3] [arg4] [arg5] [arg6]"
    (arg1: directory path to earthquake dataset, arg2: directory path to shelter dataset,
    arg3: directory path to gps dataset, arg4: directory path to road network dataset,
    arg5: directory path to osm dataset, arg6: directory path to finedust dataset)

    ex) python main.py ./earthquake_dataset/ ./shelter_dataset/ ./gps_dataset/ ./roadnetwork_dataset/ ./osm_dataset/ ./finedust_dataset/
    
    Result dataset will be saved in ./sf1_dataset_output/ folder.

* Requirements
    python pandas package: "pip3 install pandas"
    python numpy package: "pip3 install numpy"
    python geopy package: "pip3 install geopy"
    python Shapely package: "pip3 install Shapely"    
    python sklearn package: "pip3 install scikit-learn"
    python jsons package: "pip3 install jsons"



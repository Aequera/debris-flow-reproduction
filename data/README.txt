This README file describes data in the USGS Data Release: 

Graber, A.P., Gorr, A.N., Kean, J.W., Kostelnik, J., Rengers, F.K., Selander, B.D., and Thomas, M.A., 2026, USGS runoff-generated postfire debris-flow inventory: U.S. Geological Survey data release, https://doi.org/10.5066/P1R9VXC4.  


-----------------------------------------------------------------------------------------------------
---   1   Descriptions of field headers in "USGS_RG_PFDF_Inventory_v1.csv"
-----------------------------------------------------------------------------------------------------

Location, description, and timing information:
----------------------------------------------
FireName: Name of wildfire.
FireYear: Year of wildfire occurrence [yyyy].
FireIgnitionDate: Date of fire ignition for each fire. Most ignition dates were taken from the Monitoring Trends in Burn Severity wildfire database [yyyymmdd] (https://www.mtbs.gov/). Other ignition date sources used include: United States (U.S.) Forest Service Burned Area Emergency Response incident archive (https://burnseverity.cr.usgs.gov/baer/), the CalFire incident archive (https://www.fire.ca.gov/incidents), and news articles.
FireState: Abbreviation for U.S. state of wildfire occurrence. AZ = Arizona, CA = California, CO = Colorado, MT = Montana, NM = New Mexico, UT = Utah, WA = Washington, WY = Wyoming.
AssessmentFireID: Identifier for the USGS Post-Fire Debris-Flow Hazard Assessment associated with the observation, if available (King and others, 2025, https://doi.org/10.5066/P13GTMAX; King and others 2026, https://doi.org/10.5066/P14EWYME; Staley and others, 2026, https://doi.org/10.5066/P142R8E2). Refer also to Section 6 below.
AssessmentSegmentID: Stream segment identifier for the watershed where the observation was made, based on stream networks derived for USGS Post-Fire Debris-Flow Hazard Assessments, if available (King and others, 2025, https://doi.org/10.5066/P13GTMAX; King and others 2026, https://doi.org/10.5066/P14EWYME; Staley and others, 2026, https://doi.org/10.5066/P142R8E2). Refer also to Section 6 below.
UniqueObservationID: A unique identifier for each observation, using the format "FireName_FireYear_#", where "#" is an integer starting with "0001" for the first observation for a given fire and increasing for additional observations from that fire. Spaces were removed from FireNames such that the unique IDs would not have any spaces in them.
SiteName: Site name associated with the observation location, if available.
ObservationDate: Date of the observation [yyyymmdd], if available.
ObservationLatitude: Latitude of the observation [decimal degrees, WGS84, EPSG: 4326].
ObservationLongitude: Longitude of the observation [decimal degrees, WGS84, EPSG: 4326].
Response: Postfire debris-flow response [1 = Yes; 0 = No]. A “0” indicates no true debris flow was observed, but a different hydrologic response with lower sediment content may have still occurred.
ObservationSource: Name and affiliation for person(s) who provided observation and/or reference and DOI or link if previously published.
StormStart: Date of storm onset associated with the field observation [yyyymmdd].
DaysSinceFire: Number of days elapsed between fire ignition and the observed storm (that is, StormStart minus FireIgnitionDate) [days].
YearAfterFire: Year after fire in which the observed storm occurred [years]. For example, Year 1 = ignition date through 365 days after ignition. Leap years are accounted for such that 1) postfire years that incorporate a leap day are 366 days long and 2) the anniversary of the fire ignition date always begins a new year after fire.


Rainfall information:
---------------------
GageName: Name of rain gage associated with the field observation.
GageID: Station code assigned by the managing organization for the rain gage, if available.
GageLatitude: Latitude of the rain gage [decimal degrees, WGS84, EPSG: 4326], if available.
GageLongitude: Longitude of the rain gage [decimal degrees, WGS84, EPSG: 4326], if available.
GageDistance: Distance from observation/response location to rain gage location [km].
StormAccumulation: Total rainfall accumulation for the storm [mm], if available.
StormDuration: Total duration of the storm [hours], if available.
PeakI15: Peak 15-minute rainfall intensity associated with observation [mm/hr], if available.
PeakI30: Peak 30-minute rainfall intensity associated with observation [mm/hr], if available.
PeakI60: Peak 60-minute rainfall intensity associated with observation [mm/hr], if available.
1YearStormI15: 1-year recurrence interval, 15-minute rainfall intensity for the rain gage location extracted from National Oceanic and Atmospheric Administration (NOAA) precipitation atlases [mm/hr] (https://hdsc.nws.noaa.gov/pfds/). If coordinates of the rain gage were not available, this value was extracted for the observation location (that is, ObservationLatitude and ObservationLongitude).
1YearStormI30: 1-year recurrence interval, 30-minute rainfall intensity for the rain gage location extracted from NOAA precipitation atlases [mm/hr] (https://hdsc.nws.noaa.gov/pfds/). If coordinates of the rain gage were not available, this value was extracted for the observation location (that is, ObservationLatitude and ObservationLongitude).
1YearStormI60: 1-year recurrence interval, 60-minute rainfall intensity for the rain gage location extracted from NOAA precipitation atlases [mm/hr] (https://hdsc.nws.noaa.gov/pfds/). If coordinates of the rain gage were not available, this value was extracted for the observation location (that is, ObservationLatitude and ObservationLongitude).
RainfallRatio15: 15-minute rainfall ratio computed as RainfallRatio15 = PeakI15 / 1YearStormI15 [-].
RainfallRatio30: 30-minute rainfall ratio computed as RainfallRatio30 = PeakI30 / 1YearStormI30 [-].
RainfallRatio60: 60-minute rainfall ratio computed as RainfallRatio60 = PeakI60 / 1YearStormI60 [-].


Terrain variables computed for the watershed upstream of the observation location:
----------------------------------------------------------------------------------
HM23: Proportion of the watershed upstream of the observation location that was both burned at high or moderate burn severity and steeper than 23 degrees [-], if available.
dNBR/1000: Average differenced Normalized Burn Ratio of the upstream watershed divided by 1000 [-], if available.
KF-Factor: Average soil erodibility (KF-factor) [-] of the upstream watershed  extracted from the U.S. Department of Agriculture STATSGO database, if available (https://sdmdataaccess.sc.egov.usda.gov; https://doi.org/10.5066/P13WAPYV).
UpstreamArea: Contributing area of the upstream watershed [km2].


Information on inclusion in previous USGS debris-flow inventories:
------------------------------------------------------------------
PreviousUSGSInventory: Previous USGS debris-flow inventory that contained the observation, if applicable (references listed in Section 9 below). Rows with "New data, this version" were newly compiled for this version of the inventory.




-----------------------------------------------------------------------------------------------------
---   2   Note on data availability:
-----------------------------------------------------------------------------------------------------

Any cells in "USGS_RG_PFDF_Inventory_v1.csv" that contain "-9999" indicate information that is missing or does not exist.




-----------------------------------------------------------------------------------------------------
---   3   Note on data sorting:
-----------------------------------------------------------------------------------------------------

Rows in "USGS_RG_PFDF_Inventory_v1.csv" are sorted first by FireName, then by AssessmentSegmentID, then by StormStart.




-----------------------------------------------------------------------------------------------------
---   4   Note on FireIgnitionDate values for the Grand Prix and Old Fires:
-----------------------------------------------------------------------------------------------------

For the purposes of hazard assessment by USGS, the Grand Prix and Old Fires (2003, California) were treated together, and their debris-flow data are grouped together. For all records from Grand Prix - Old, the listed FireIgnitionDate is 20031025, which is the ignition date of the Old Fire. The Grand Prix Fire ignited slightly earlier on 20031021.




-----------------------------------------------------------------------------------------------------
---   5   Notes on data selection for the 2012 Whitewater-Baldy and 2019 Woodbury Fires:
-----------------------------------------------------------------------------------------------------

1)  The debris-flow entries in this compilation taken from the 2012 Whitewater-Baldy Fire include only debris flows that met both of these conditions as flagged in the original sources (Tillery and others, 2019; Tillery and Rengers, 2020): 1) They were generated by distributed runoff initiation (excluding those initiated by runoff waterfalling off bedrock ledges, that is, "firehose" initiation) and 2) they initiated within the burned area. The original dataset published by Tillery and others (2019) and Tillery and Rengers (2020) includes many more debris flows that were initiated by mechanisms other than distributed runoff and/or were mapped outside the burned area.

2)  The debris-flow entries in this compilation taken from the 2019 Woodbury Fire include only observations taken from burned catchments, as flagged in the original source (McGuire and others, 2021).




-----------------------------------------------------------------------------------------------------
---   6   Note on values in the AssessmentFireID column:
-----------------------------------------------------------------------------------------------------

The formatting for AssessmentFireID values associated with USGS Post-Fire Debris-Flow Hazard Assessments (https://usgs.maps.arcgis.com/apps/dashboards/c09fa874362e48a9afe79432f2efe6fe) has changed through time. Early assessments (for example, before 2013) generally used identifiers of only two or three letters (for example, "cs" for the 2002 "Coal Seam Fire"). From 2017 to early 2025, fires were assigned identifiers of three letters followed by an underscore and the year the fire ignited (for example, "elk_2024" for the 2024 Elk Fire). From mid 2025 onward, the FireID was extended to include the fire name, the date of ignition and the assessment version number separated by underscores (for example, "Lee_2025-08-02_v1.0" for the version 1 assessment for the 2025 Lee Fire). Assessment shapefiles for most of the fires represented in the present inventory are available from one of the following repositories.

King, J.M., Kostelnik, J., and Kean, J.W., 2025, 2024 Post-Wildfire Debris-Flow Hazard Assessments: U.S. Geological Survey data release, https://doi.org/10.5066/P13GTMAX.

King, J.M., Kostelnik, J., Kean, J.W., Barnhart, K.R., Graber, A.P., Rengers, F.K., and Thomas, M.A., 2026, Post-Wildfire Debris-Flow Hazard Assessment (PWFDF) Collection: U.S. Geological Survey data release, https://doi.org/10.5066/P14EWYME.

Staley, D.M., Kean, J.W., Kostelnik, J., King, J.M., Jones, E.S., Schmitt, R.G., Rengers, F.K., Thomas, M.A., and Negri, J., 2026, 2013 - 2023 Post-Wildfire Debris-Flow Hazard Assessments: U.S. Geological Survey data release, https://doi.org/10.5066/P142R8E2.




-----------------------------------------------------------------------------------------------------
---   7   Notes on changes applied to the inventory of Staley et al. (2016):
-----------------------------------------------------------------------------------------------------

We applied small changes to the inventory of Staley et al. (2016) to correct minor errors. These changes resolved the following issues:

1)  Incorrect values in the StormDate column of Staley et al. (2016) that did not agree with the StormStart (which gives the exact timing for the beginning of rainfall), including some StormDates that  preceded the fire ignition. 
2)  Incorrect FireYears for Jesusita and Horseshoe 2 fires.
3)  Incorrect storm years associated with 11 records for the 2009 Station Fire. For a few records, storms on December 9 and January 16 were incorrectly listed with the years 2005 and 2006, respectively. The relevant records have been corrected to 2009 and 2010, respectively.
4)  Incorrect FireState for the Bear Fire. The FireState was previously listed as Idaho, but has been corrected to Montana.
5)  Incorrect soil KF-Factor values for 4 records from the Little Bear Fire and 1 record from the Cerro Grande Fire.
6)  Incorrect UpstreamArea values for a few watersheds from the Buckweed, Coal Seam, Grand Prix - Old, Little Bear, Monument, Purdy Creek, Santiago, Station, Sula Complex (Maynard), and Witch Fires.
7)  Incorrect or missing rainfall statistics (PeakI15, PeakI30, PeakI60, StormAccumulation, StormDuration) for some records from the Schultz and Monument Fires, which we corrected, where possible, using updated values from Fernandez Sirgo and others (2026).


In addition to addressing the errors above, we made a few other minor revisions to the Staley et al. (2016) inventory to update it for the present data release:  

1)  Reformatting storm dates to YYYYMMDD.
2)  Converting UTM observation coordinates to Lat/Lon (WGS 84). 
3)  Converting gage distances from m to km.
4)  Removing records for the Sesnon Fire and select negative observations (that is, Response = 0) from the Station fire, since these entries were missing all three (15-, 30-, and 60-minute) rainfall intensities. The original Staley et al. (2016) inventory contained 1550 records. With removal of these records, 1435 records remain and are reproduced in the present data release.
5)  Modifying the FireNames for the Bear, Freeway, Fridley Peak, Purdy, and Sula Fires to match the entries for these fires on the MTBS database so future users can more easily identify these fires. These are now named Valley Complex (Bear), Freeway Complex, Fridley, Purdy Creek, and Sula Complex (Maynard) respectively. 
6)  Flagging missing data with “-9999” instead of “NaN”. 




-----------------------------------------------------------------------------------------------------
---   8   Notes on decimal places and significant digits:
-----------------------------------------------------------------------------------------------------

Precision reported in the "USGS_RG_PFDF_Inventory_v1.csv" file is variable because different datasets included in this compilation provided different levels of precision.

1)  All GPS coordinates (in the fields: ObservationLatitude, ObservationLongitude, GageLatitude, GageLongitude), were rounded to 6 decimal places. If fewer than six decimal places are visible in a given coordinate, this indicates that the original data source reported GPS coordinates to fewer than 6 decimal places. Trailing zeros (for example, the "0" in "38.6380") were not retained.

2)  For the GageDistance field, data were rounded to 3 decimal places, though 3 decimal places of precision was not available for every dataset. Trailing zeros (for example, the "0" in "3.20") were not retained.

3)  The number of significant digits for the StormAccumulation, StormDuration, PeakI15, PeakI30, and PeakI60 fields is variable. All rainfall intensities, storm durations, and storm accumulations were rounded to 1 decimal place, rather than choosing a fixed number of significant digits. This approach was chosen because the appropriate number of significant digits is often unknown for these fields (for example, the measurement uncertainties of many of the rain gages in this inventory are unknown). In addition, the rainfall intensities and storm accumulations reported here vary over 4 orders of magnitude. Therefore, if a fixed, small number of significant digits (for example, 2) was used, large intensities would change noticeably due to rounding. But if a larger number of significant digits (for example, 4) was used, then rainfall measures for small storms would be reported to several decimal places, implying more precision than is probably reasonable. Trailing zeros (for example, the "0" in "3.0") were not retained.

4)  One-year recurrence interval storm intensities (1YearStormI15, 1YearStormI30, 1YearStormI60) and rainfall ratios (RainfallRatio15, RainfallRatio30, RainfallRatio60) were rounded to 2 decimal places. Trailing zeros (for example, the "0" in "9.90") were not retained.

5)  Fire and terrain variables (HM23, dNBR/1000, KF-Factor, and UpstreamArea) were rounded to 4 decimal places. Trailing zeros (for example, the second "0" in "0.3610") were not retained.




-----------------------------------------------------------------------------------------------------
---   9   Prior USGS debris-flow inventories that are reproduced in this inventory:
-----------------------------------------------------------------------------------------------------

Graber, A.P., 2023, Compilation of runoff-generated debris-flow inventories for 17 fires across Arizona, California, Colorado, New Mexico, and Washington, USA: U.S. Geological Survey data release, https://doi.org/10.5066/P98Q4CDH.  

Graber, A.P., 2024, Compilation of runoff-generated debris-flow inventories for 18 fires across Arizona, California, Colorado, New Mexico, Utah, and Washington, USA: U.S. Geological Survey data release, https://doi.org/10.5066/P13ZFKJS.

Rengers, F.K., Bower, S.J., Knapp, A., Kean, J.W., and Staley, D.M., 2023, Debris Flow, Precipitation, and Volume Measurements in the Grizzly Creek Burn Perimeter June 2021-September 2022, Glenwood Canyon, Colorado (Version 1.1): U.S. Geological Survey data release. https://doi.org/10.5066/P9Z7RROL.

Staley, D.M., Negri, J.A., Kean, J.W., Laber, J.M., Tillery, A.C., and Youberg, A.M., 2016, Updated logistic regression equations for the calculation of post-fire debris-flow likelihood in the western United States (U.S. Geological Survey Open-File Report 2016–1106, 13 p.), U.S. Geological Survey, https://doi.org/10.3133/ofr20161106.

Thomas, M.A., Lindsay, D.N., Cavagnaro, D.B., Kean, J.W., McCoy, S.W., and Graber, A.P., 2023a, Field-verified inventory of post-fire debris flows for the 2021 Dixie Fire following a 23-25 October 2021 atmospheric river storm and 12 June 2022 thunderstorm: U.S. Geological Survey data release, https://doi.org/10.5066/P9YPX1BM.

Thomas, M.A., Kean, J.W., McCoy, S.W., Lindsay, D.N., Kostelnik, J., Cavagnaro, D.B., Rengers, F.K., East, A.E., Schwartz, J.Y., Smith, D., and Collins, B.D., 2023b, Field-verified inventory of postfire hydrologic response for the 2020 CZU Lightning Complex, River, Camel, and Dolan Fires following a 26-29 January 2021 atmospheric river storm sequence: U.S. Geological Survey data release, https://doi.org/10.5066/P91O03Y7. 




-----------------------------------------------------------------------------------------------------
---   10   Other references that provided debris-flow and/or rainfall information for this inventory:
-----------------------------------------------------------------------------------------------------

Beers, R., Robichaud, P., Youberg, A., McGuire, L., Joyal, T., Porter, R., Loverich, J., Schenk, E., and Gorr, A., 2023, 2019 Museum Fire Geomorphic Recovery and Post-Fire Flooding Implications [recorded presentation]: Southwest Fire Science Consortium, accessed July 09, 2024, at https://www.swfireconsortium.org/2022/12/22/geomorphology_museumfire/.

Cavagnaro, D., McCoy, S.W., Lindsay, D.N., McGuire, L.A., and Trugman, D., 2024, Supporting data for: "Rainfall thresholds for postfire debris-flow initiation vary with short-duration rainfall climatology" (Version 5), figshare, https://doi.org/10.6084/m9.figshare.25569603.v5.

Cavagnaro, D.B., McCoy, S.W., Lindsay, D.N., McGuire, L.A., Kean, J.W., and Trugman, D.T., 2025, Rainfall Thresholds for Postfire Debris-Flow Initiation Vary With Short-Duration Rainfall Climatology. Journal of Geophysical Research: Earth Surface, 130, e2024JF007781,  https://doi.org/10.1029/2024JF007781. 

DeGraff, J.V., Staley, D.M., Stock, G.M., Takenaka, K., Gallegos, A.L., and Neptune, C.K., 2022, Rainfall triggering of post-fire debris flows over a 28-year period near El Portal, California, USA. Environmental and Engineering Geoscience, 28(1), 133-145, https://doi.org/10.2113/EEG-D-21-00031. 

East, A.E., Logan, J.B., Dartnell, P., Lieber-Kotz, O., Cavagnaro, D.B., McCoy, S.W., and Lindsay, D.N., 2021, Watershed Sediment Yield Following the 2018 Carr Fire, Whiskeytown National Recreation Area, Northern California. Earth and Space Science, 9, e2021EA001828,  https://doi.org/10.1029/2021EA001828. 

East, A., Logan, J., Dartnell, P., Lieber-Kotz, O., Cavagnaro, D., McCoy, S., and Lindsay, D., 2021, Carr Fire post-fire precipitation and topographic data, Hydroshare, http://www.hydroshare.org/resource/e2279e8f277449bc8fb878b592931ef3.

East, A.E., and Williamson, J.L., 2023, Rain measurements in the Dolan Fire Area, Los Padres National Forest, California, 2021 to 2022: U.S. Geological Survey data release, https://doi.org/10.5066/P9VVYKJ7. 

Fernandez Sirgo, A.I., McGuire, L.A., Youberg, A.M., and Liu, T., 2026, Predictive models for postfire debris flow initiation in the southwest USA. Journal of Geophysical Research: Earth Surface, 131, 6, e2025JF008627. https://doi.org/10.1029/2025JF008627.

Friedman, E.Q., and Santi, P.M., 2014, Debris-flow hazard assessment and validation following the Medano Fire, Great Sand Dunes National Park and Preserve, Colorado. Landslides, 11, 1093-1113, https://doi.org/10.1007/s10346-013-0462-9. 

Friedman, E.Q., and Santi, P.M., 2019, Relationship between rainfall intensity and debris-flow initiation in a southern Colorado burned area. In J.W. Kean, J.A. Coe, P.M. Santi, B.K. Guillen (Eds.), Proceedings of the 7th International Conference on Debris-Flow Hazards Mitigation, Golden, CO, 10-13 June 2019, http://dx.doi.org/10.25676/11124/173181.
 
Gorr, A.N., McGuire, L.A., Beers, R., and Hoch, O.J., 2023, Triggering conditions, runout, and downstream impacts of debris flows following the 2021 Flag Fire, Arizona, USA: Natural Hazards, v. 117, p. 2473-2504, https://doi.org/10.1007/s11069-023-05952-9. 

Gorr, A.N., McGuire, L.A., Youberg, A.M., Beers, R., and Liu, T., 2024, Inundation and flow properties of a runoff-generated debris flow following successive high-severity wildfires in northern Arizona, USA: Earth Surfaces Processes and Landforms, v. 49, no. 2, p. 622-641, https://doi.org/10.1002/esp.5724. 

Kean, J.W., Staley, D.M., Rengers, F.K., McGuire, L.A., Smith, J.B., and Mirus, B.B., 2018, Post-wildfire debris-flow monitoring data, 2014 Silverado Fire, Orange County, California, November 2014 to January 2016: U.S. Geological Survey data release, https://doi.org/10.5066/F70K27R0. 

McGuire, L.A., Rengers, F.K., Kean, J.W., Staley, D.M., and Mirus, B.B., 2018, Incorporating spatially heterogeneous infiltration capacity into hydrologic models with applications for simulating post-wildfire debris flow initiation: Hydrological Processes, v. 32, p. 1173-1187, https://doi.org/10.1002/hyp.11458. 

McGuire, L., 2021, Buzzard-Pinal-Fish Fires recovery dataset, HydroShare,  http://www.hydroshare.org/resource/96351adbdacc45e793d8fb5a740d8ac4.

McGuire, L.A., Youberg, A.M., Rengers, F.K., Abramson, N.S., Ganesh, I., Gorr, A.N., Hoch, O., Johnson, J.C., Lamom, P., Prescott, A.B., Zanetell, J., and Fenerty, B., 2021, Post-wildfire debris-flow monitoring data, 2019 Woodbury Fire, Superstition Mountains, Arizona, USA November 2019 to February 2020: U.S. Geological Survey data release, https://doi.org/10.5066/P9URVNXI.

McGuire, L.A., Rengers, F.K., Youberg, A.M., Gorr, A.N., Hoch, O., and Beers, R., 2024, Hydrologic monitoring and field data collected following the 2020 Tadpole Fire, New Mexico, USA: HydroShare, https://doi.org/10.4211/hs.136eeec98a4141e6aedb57bdf6fb1fb5. 

Michel, A., Kean, J.W., Smith, J.B., Allstadt, K.E., and Coe, J.A., 2019, Taking the pulse of debris flows: Extracting debris-flow dynamics from good vibrations in southern California and central Colorado. In J.W. Kean, J.A. Coe, P.M. Santi, and B.K. Guillen (Eds.), Debris-Flow Hazards Mitigation: Mechanics, Monitoring, Modeling, and Assessment (AEG Special Publication 28, pp. 154-161), Association of Environmental and Engineering Geologists, https://doi.org/10.25676/11124/173224. 

Neptune, C.K., DeGraff, J.V., Pluhar, C.J., Lancaster, J.T., and Staley, D.M., 2021, Rainfall thresholds for post-fire debris-flow generation, Western Sierra Nevada, CA: Environmental and Engineering Geoscience, v. 27, no. 4, p. 439-453, https://doi.org/10.2113/EEG-D-21-00039.

Porter, R., Joyal, T., Beers, R., Youberg, A., Loverich, J., Schenk, E., and Robichaud, P.R., 2023, Characterization of Environmental Seismic Signals in a Post-Wildfire Environment – Examples From the Museum Fire, AZ: Journal of Geophysical Research: Earth Surface, v. 128, article e2022JF006962, https://doi.org/10.1029/2022JF006962. 

Rengers, F.K., McGuire, L.A., Kean, J.W., Staley, D.M., Dobre, M., Robichaud, P.R., and Swetnam, T., 2021, Movement of sediment through a burned landscape: Sediment volume observations and model comparisons in the San Gabriel Mountains, California, USA. Journal of Geophysical Research: Earth Surface, 126, e2020JF006053, https://doi.org/10.1029/2020JF006053. 

Skene, F.E., Rengers, F.K., Thomas, M.A., Hoch, O.J., and Kean, J.W., 2024a, Rainfall, Volumetric soil-water content, Video, and Geophone Data from the Calwood Fire Burn Area, Colorado, April 2021 to November 2023: U.S. Geological Survey data release, https://doi.org/10.5066/P1ZTPZPW.

Skene, F.E., Rengers, F.K., Hoch, O.J., Kean, J.W., and Thomas, M.A., 2024b, Rainfall, Volumetric Soil-Water Content, Video, and Geophone Data from the Hermits Peak-Calf Canyon Fire Burn Area, New Mexico, June 2022 to June 2024: U.S. Geological Survey data release, https://doi.org/10.5066/P13WVRUX. 

Swanson, B.J., Lukashov, S.G., Schwartz, J.Y., Lindsay, D.N., and Lancaster, J.T., 2022, Assessment of logistic regression model performance and physical controls on January 9, 2018, debris flows, Thomas Fire, California. Environmental and Engineering Geoscience, 28(1), 113-131, https://doi.org/10.2113/EEG-D-21-00026. 

Swanson, B.J., Lindsay, D.N., Cato, K., DiBiase, R.A., and Neely, A.B., 2024, Debris flows and sediment transport at Yucaipa Ridge and impacts to Oak Glen and Forest Falls area, southern California, following the 2020 El Dorado and Apple Fires. In N.J. Van Buer, J.J. Schwartz (Eds.), From Coastal Geomorphology to Magmatism: Guides to GSA Connects 2024 Field Trips in Southern California and Beyond (Geological Society of America Field Guide 70, pp. 45-73), Boulder, CO: Geological Society of America, https://doi.org/10.1130/2024.0070(03). 

Tang, H., McGuire, L.A., Rengers, F.K., Kean, J.W., Staley, D.M., and Smith, J.B., 2019, Evolution of debris-flow initiation mechanisms and sediment sources during a sequence of postwildfire rainstorms. Journal of Geophysical Research: Earth Surface, 124, 1572-1595, https://doi.org/10.1029/2018JF004837.

Tillery, A.C., and Rengers, F.K., 2020, Controls on debris-flow initiation on burned and unburned hillslopes during an exceptional rainstorm in southern New Mexico: Earth Surface Processes and Landforms, v. 45, p. 1051-1066, https://doi.org/10.1002/esp.4761.

Tillery, A.C., Rengers, F.K., and Mitchell, A.C., 2019, Post-wildfire debris flow and rainfall data, Whitewater-Baldy complex fire, southwestern New Mexico: U.S. Geological Survey data release, https://doi.org/10.5066/P90C629B. 
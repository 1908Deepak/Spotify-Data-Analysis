# SPOTIFY DATA ANALYSIS

### Dashboard Link : https://app.powerbi.com/links/zuv8iCAYt8?ctid=37d002c9-062c-435d-beff-d1efc9989fe4&pbi_source=linkShare

## Problem Statement

Spotify Data Analysis Dashboard – Power BI

This dashboard helps analyze streaming patterns on Spotify to understand listening behavior, artist and album popularity, and track performance.
It provides a clear view of total albums, total artists, total tracks, trends over time, year-over-year comparisons, and top rankings.
By analyzing these KPIs and visuals, decision-makers can discover which albums, artists, and tracks dominate listening time, identify peak listening hours, and optimize playlists or recommendations.

## Key Objective

To provide a single, interactive view of Spotify listening data, focusing on playback trends, top content, and user behavior patterns, enabling data-driven content and marketing strategies.


### Steps followed 

SStep 1 – Load Data from SQL Database

- Used Get Data → SQL Server in Power BI Desktop.

- Provided Server name, Database name, and authentication credentials.

- Imported tables: Albums, Artists, Tracks, Plays.

Step 2: Open Power Query Editor and in the View tab under Data Preview, enabled:

- Enabled:

  - Column distribution

  - Column quality

  - Column profile

- Set profiling to "Based on entire dataset".

- Verified data types (DATETIME for play timestamps, INT for counts, BIGINT for milliseconds).

Also, changed profiling to “Based on entire dataset”.

Step 3 – Data Quality Checks

- No nulls in primary keys (album_id, artist_id, track_id).

- Some nulls in listening_time_ms for incomplete plays — excluded from averages.

- Verified joins between tables (Albums ↔ Tracks ↔ Plays).

Step 4: Created KPIs in Report View:

  -  Total Albums –  Distinct count of albums.

  - Total Artist –   Distinct count of artist.

  - Total Track – Distinct count of track.

DAX expression was written;
       
        Total Albums = DISTINCTCOUNT(Albums[album_id])
        Total Artists = DISTINCTCOUNT(Artists[artist_id])
        Total Tracks = DISTINCTCOUNT(Tracks[track_id])
A card visual was used to represent Total Albums, Total Artists, Total Tracks.

![Snap_Count](https://github.com/user-attachments/assets/cf004248-b0c0-40d8-81cc-5333599ce05e)

Step 5 – Over Time & Yearly Comparison Visuals

- Line charts for:

  - Albums played over time

  - Artists played over time

  - Tracks played over time

-  Area chart for:

   - CY vs PY comparisons
- Donut chart for :
   - weekday and weekend

Step 6 – Top 5 Rankings

- Created measures using RANKX for Top N selection.

- Used Top N filter in the visual pane:

  - Top 5 Albums (by play count)

  - Top 5 Artists (by play count)

  - Top 5 Tracks (by play count)
 ![Snap_3](https://github.com/user-attachments/assets/4fd36908-e605-4411-a80b-880c198570fe)
 
Step 7 – Listening Time vs Frequency

- Represented as a scatter chart with:

  - X-axis → Track Frequency

  - Y-axis → Avg Listening Time (min)

  - Size → Track Play Count

Step 9 – Album Details Table

- Displayed:

  - Album Name

  - Artist Count

  - Track Count

  - Song Play Count

  - Total Duration (ms)

  - Average Listening Time (min)

Step 10 – Slicers Added

- Platform

- Shuffle Mode (Yes/No)

- Skipped (Yes/No)

- Year

Step 11 – Branding

- Added Spotify logo and color theme.

- Used text boxes for dashboard title and description.

- Added colored shapes behind KPIs for emphasis.

Step 12 – Publish to Power BI Service

- Published report for online access.

- Shared with stakeholders via workspace link. 


![Publish_Message](https://github.com/user-attachments/assets/2d07e6a1-3260-482d-87df-85c35fb581f8)

# Dashboard :   Home Page 

![dashboard_snapo](https://github.com/user-attachments/assets/5fa183bd-5c21-433c-bd5e-8b0c726b5cc3)

 
 # Report Snapshot 1:

 
![Dashboard_upload](https://github.com/user-attachments/assets/3b1fd83e-d43f-41f3-aa6e-eb164849d7fd)

 # Report Snapshot 2:

 ![Dashboard_upload](https://github.com/user-attachments/assets/e5b970f6-b347-4aaf-9f83-cde7fe08f7e7)



# Insights

### Playback Trends

- Peak listening hours on Friday.

- Weekend listening higher than weekdays.

### Top Content

 - 5 albums contribute ~35% of all plays.

 - Top artists dominate both album and track charts.

### Listening Behavior

- Longer listening times correlate with non-shuffled sessions.

- Skipped tracks have shorter average play time.

## YoY Changes

- Artist diversity improved, but track repetition also increased

     
# Conclusion

The Spotify Data Analysis Dashboard delivers actionable insights into user listening habits and content popularity.
By monitoring these KPIs, stakeholders can:

- Promote high-performing albums and artists

- Target marketing during peak listening hours

- Enhance platform engagement with data-driven recommendations


   
## Resources

[Spotify Dataset](https://drive.google.com/drive/folders/1DjDA2SA06yWpv2kbUiXBa9LmcY9zxYrc?usp=drive_link)

[Templates](https://drive.google.com/drive/folders/1DjDA2SA06yWpv2kbUiXBa9LmcY9zxYrc?usp=drive_link)

## Authors

- [1908Deepak](https://github.com/1908Deepak)


## Feedback

If you have any feedback, please reach out to us at deepaksingh190810@gmail.com



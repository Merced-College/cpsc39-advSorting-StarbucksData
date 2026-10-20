# Start here: Caffeine Quest student project

1. Extract the ZIP. In Eclipse select **File > Import > General > Existing Projects into Workspace**.
2. Choose the extracted **CaffeineQuestStudent** folder. Import the project of that name.
   It is separate from the instructor project, CaffeineQuest.
3. Use an installed **JDK 11 or newer**. No Maven or extra Java libraries are required.
4. Expand **src > caffeinequest**, right-click **CaffeineQuest.java**, and choose
   **Run As > Java Application**.
5. Click inside the Console. Press Enter for mode **1 (Demo)** and each default.
   This uses approximate central Merced coordinates and displays the closest ten stores.
   Press Enter at the final repeat prompt to finish.
6. Right-click **MapPreviewServer.java > Run As > Java Application**. Keep it running.
7. Open **http://localhost:8080/demo-map.html** in your normal web browser.
   Use this address, rather than double-clicking the HTML file. The map needs internet.
8. Read **ASSIGNMENT.md**. Complete TODO A-D in **MergeSort.java**.
9. Run **SortCheck.java > Run As > Java Application** to check your implementation.
10. Run CaffeineQuest again and choose **2 (Student)**. Once it completes, open
    **http://localhost:8080/student-map.html**. The two modes save separate map files.

Each map displays its sorting mode so you can identify your evidence. Demo works
before the TODOs are done. Student mode deliberately reports an unfinished merge
and does not export a Student map until you implement it. SortCheck initially
reports failures; this is expected. Never copy the Demo sort into MergeSort.

## Troubleshooting

- **File not found:** Run > Run Configurations > Java Application > select the
  affected application > Arguments > Working directory > Other > Workspace >
  choose **CaffeineQuestStudent**. Do this for CaffeineQuest, SortCheck, and the
  preview server if needed.
- **Red server imports:** This project includes `src/module-info.java` with
  `requires jdk.httpserver;`. Keep it. Make sure Eclipse uses a full JDK 11+.
- **Port 8080 already in use:** Stop the old preview server with the Console's
  red square before starting this one. The server intentionally keeps running.
- **Map shows 404:** Generate the matching Demo or Student map first, then refresh.
- **Map tiles blocked:** Use the localhost address. If still blocked, tell your
  instructor; browser/network restrictions can also affect external map requests.
- **Old results:** Each search overwrites that mode's map. Refresh the browser
  after a new search. Save copies/screenshots for evidence when you change inputs.
- **No output folder visible in Eclipse:** Right-click the project > Refresh.

## Files

| File | Role | Your work |
|---|---|---|
| MergeSort.java | Recursive sort with unfinished merge | Complete TODO A-D |
| CaffeineQuest.java | Console menu, filtering, mode selection | Possible customization |
| StoreDistance.java | Distance calculation and comparator | Research / possible customization |
| StarbucksStore.java | Store data model | Supplied |
| CsvLoader.java | Reads the supplied CSV | Supplied / research option |
| MapExporter.java | Embeds ranked data in HTML | Supplied / research option |
| MapPreviewServer.java | Serves map pages locally | Supplied / research option |
| SortCheck.java | Correctness checks with built-in sort oracle | Run; keep unchanged |
| resources/map-template.html | Map and ranked cards | Supplied / research option |
| REFLECTION-TEMPLATE.md | Planning and submission prompts | Complete |

Data is a course snapshot, not a live store directory. Distances are straight-line
miles, not driving routes. Default coordinates are approximately central Merced,
not verified Merced College coordinates. Unfiltered data has 2,558 records;
the drive-through filter matches 577. Map tiles are loaded only as normally viewed;
do not add bulk downloads or remove attribution.

Technical references for supplied map infrastructure:
https://leafletjs.com/examples/quick-start/
https://operations.osmfoundation.org/policies/tiles/

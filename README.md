# The Geometry of College Fight Songs

This interactive dashboard (live at valkobarnabas.github.io) uses D3.js to visualize the lyrical and musical make-up of fight songs. Clicking any node or logo analyzes that school's fight song, activating a central info panel which displays the title, author and origin of the song, and an embedded Spotify player of the specified song.

The dashboard contains four distinct data visualizations:

1) The TROPE-O-METER (top left) quantifies lyrical clichés. Hovering over a trope icon defines the trope and highlights schools that use it. Clicking a logo illuminates that specific song's tropes; otherwise, aggregate usage is shown.

2) The JACCARD NETWORK (top right) is a network graph that connects songs by similar tropes. Treating the tropes of songs as sets, we use the Jaccard index as a measure of similarity. Hovering over or clicking a node reveals links to its "neighbors" (songs with ≥75% trope similarity).

3) SONG TOPOLOGY (bottom left) plots tempo (BPM) vs. duration with added density contours. Node color indicates how many times the word "fight" is sung. 

4) ORIGIN STORY (bottom right) is an UpSet plot showing how songs were created based off the power set of {Student Author, Contest Winner, Official Song}. Hovering over bars highlights songs with corresponding origins.

The dashboard is designed to be intuitive and responsive, and has keyboard shortcuts for fullscreen ('F') and accessible high-contrast mode ('A'). Tooltips provide further context on mouseovers, and icons are used to promote ease of comprehensibility.

[Link to dashboard!](https://valkobarnabas.github.io) *(does not currently support mobile)*

## Background

[Bucky’s Data Viz Challenge](https://data.wisc.edu/love-data-week/buckys-data-viz-challenge/) is an annual data visualization competition put on by the University of Wisconsin-Madison.
One winner goes on to represent the Badgers at the annual [Big Ten Academic Alliance (BTAA) Data Viz Championship](https://btaa.org/technology/love-data-week/data-viz-student-championship).

The 2026 edition of the championship revolves around college fight songs. 
The dataset of 65 songs, adapted from FiveThirtyEight's [Fight Song Dataset](https://github.com/fivethirtyeight/data/blob/master/fight-songs/fight-songs.csv), includes data points regarding various tropes present in the fight songs (saying the words "fight" or "rah," for instance), as well as musical attributes such as
tempo and duration. Also included is the origin of the song, including author, year written, and whether a contest took place to establish the fight song, and a corresponding Spotify ID of the song.

## Resources used

* [D3.js](https://d3js.org/) for data visualization framework.
* [FontAwesome](https://fontawesome.com/) for icons.
* The [Segoe UI](https://fonts.adobe.com/fonts/segoe-ui) font family.
* The website [d3indepth.com](d3indepth.com), for its very helpful tutorials on D3.js.
* [This post](https://www.audioeye.com/post/8-ways-to-design-a-color-blind-friendly-website/) from audioeye.com, for its guideline on designing accessible websites.
* All text was written by the author. The artificial intelligence tool Google Gemini 3 was used sparingly and under careful cross-checking to troubleshoot bugs in code.

## Author Information
Barnabás Valkó (bvalko@wisc.edu) is a Junior at the University of Wisconsin-Madison studying Mathematics (B.S.), Statistics (B.S), Physics (Cert.), and Educational Policy Studies (Cert.).




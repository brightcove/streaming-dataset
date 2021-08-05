Brightcove Streaming Datasets
=============================

This project contains several examples of real-world streaming playback statistics provided for academic research purposes.
The description of this data set and possible examples of its use are explained in papers:

* T. Teixeira, B. Zhang, Y. Reznik, "Adaptive Streaming Playback Statistics Dataset," Proc. 12th ACM Multimedia Systems Conference (MMSys '21), Istanbul, Turkey. September 28-October 1, 2021. [DOI 10.1145/3458305.3478444](https://doi.org/10.1145/3458305.3478444)

* Y. Reznik, K. Lillevold, A. Jagannath, and X. Li, "Towards Understanding of the Behavior of Web Streaming,"  Proc. The Picture Coding Symposium (PCS'21), Bristol, UK, June 29 - July 2, 2021.

This material is shared under Apache License Version 2.0, with the full text of the license provided in file [LICENSE](./LICENSE).


## Explanation of parameters/data fields provided in the data set:
Files are organized in directories, one for each event. Files inside those directories are organized with the following naming convention:

`eventX_playback_statistics_Y.csv`

where `X` is the event number or identification and `Y` is the file number breakdown for each event to accommodate GitHub's limitation of 100 MB file size.

Each file contains the following columns:

<table>
<thead>
  <tr>
    <th>Category</th>
    <th>Parameter</th>
    <th>Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">session</td>
    <td>session</td>
    <td>Randomly generated number associated with each player session</td>
  </tr>
  <tr>
    <td>seq</td>
    <td>Sequential number of an event within a session</td>
  </tr>
  <tr>
    <td rowspan="6">client</td>
    <td>device_type</td>
    <td>Device type. Possible values: “desktop”, “mobile”, “tablet”, “tv”, “other”</td>
  </tr>
  <tr>
    <td>device_os</td>
    <td>OS type. Possible values: “windows”, “osx”, “linux”, “android”, “ios”, ”webos”, ”other”</td>
  </tr>
  <tr>
    <td>browser	</td>
    <td>Browser type. Possible values: “chrome”, “firefox”, “safari”, “edge”, “ie”, “opera”, “other”</td>
  </tr>
  <tr>
    <td>player</td>
    <td>Player type. Possible values: “app” – dedicated application, “web” – JS / browser-based player</td>
  </tr>
  <tr>
    <td>player_width</td>
    <td>Player window width [pixels]</td>
  </tr>
  <tr>
    <td>player_height</td>
    <td>Player window height [pixels]</td>
  </tr>
  <tr>
    <td rowspan="8">rendition</td>
    <td>rendition_indicated_bps</td>
    <td>Rendition bitrate [bps]. Sum of audio and video bitrates.</td>
  </tr>
  <tr>
    <td>rendition_width</td>
    <td>Video width as encoded [pixels]</td>
  </tr>
  <tr>
    <td>rendition_height</td>
    <td>Video height as encoded [pixels]</td>
  </tr>
  <tr>
    <td>rendition_framerate</td>
    <td>Video framerate [fps]</td>
  </tr>
  <tr>
    <td>video_codec	</td>
    <td>Video codec type. Possible values: “h264”, “hevc”, “av1”</td>
  </tr>
  <tr>
    <td>video_codec_profile</td>
    <td>Video codec profile. Possible values: “baseline”, “main”, “high”</td>
  </tr>
  <tr>
    <td>format</td>
    <td>Streaming format. Possible values: “hls_v3”, “hls_v7”, “dash”</td>
  </tr>
  <tr>
    <td>segment_duration</td>
    <td>Segment duration [seconds]</td>
  </tr>
  <tr>
    <td rowspan="5">playback</td>
    <td>video_seconds_viewed</td>
    <td>Seconds of media content played in the period between the last two player events </td>
  </tr>
  <tr>
    <td>forward_buffer_seconds</td>
    <td>The number of seconds of media content buffered but not yet played</td>
  </tr>
  <tr>
    <td>rebuffering_seconds</td>
    <td>The total number of seconds the player was “buffering” in the period between the last two player events</td>
  </tr>
  <tr>
    <td>rebuffering_count</td>
    <td>The number of times the player was “buffering” in the period between the last two player events</td>
  </tr>
  <tr>
    <td>media_bytes_transferred</td>
    <td>The total number of bytes transferred since the start of the session</td>
  </tr>
  <tr>
    <td>network</td>
    <td>measured_bps</td>
    <td>Network bandwidth [bps] estimated based on size and delivery time of the last segment downloaded</td>
  </tr>
</tbody>
</table>


# Citing our Work

If you found the datasets useful and used in your research, we kindly ask that you would reference the following paper:

T. Teixeira, B. Zhang, Y. Reznik, "Adaptive Streaming Playback Statistics Dataset," Proc. 12th ACM Multimedia Systems Conference (MMSys '21), September 28-October 1, 2021, Istanbul, Turkey

## Contact the Authors

Thiago Teixeira (tteixeira at brightcove dot com)<br>
Bo Zhang<br>
Yuriy Reznik<br>

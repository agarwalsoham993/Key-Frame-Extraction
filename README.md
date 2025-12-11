# Key-Frame-Extraction

For Extracting the key frames out of the video.

## Current Pipeline :
Extraction of video frames -> Calculation of differences -> creating clusters based on maxima's -> Clustering of images to reduce redundancy -> Choosing the best shot from clusters (using brightness and laplacian scores.
## 
- first selecting the frames with maximum change among the `"len window"` (here 10)
   - the local maxima calculation required multiple steps to be performed alongside like smoothing and maxima calculation.
- for the key frames extraction from the selected `candidate frames` we need to follow multiple steps like
  - Performing `HDBscan` clustering for the images to cluster similar images or multiple frames of the same scene together
  - extracting the frame with optimal brightness, contrast, and least amount of Blur (`using laplacian score`) from the cluster.

We will follow ahead with Time Series Analysis ,LSTM , and other Machine Learning pipelines for extracting the key frames from a video.

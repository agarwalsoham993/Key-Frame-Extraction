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

## Sample video results
<img width="1745" height="1430" alt="image" src="https://github.com/user-attachments/assets/c23563b7-182c-4238-86d0-42a522ba61b6" />


## <img width="1536" height="208" alt="image" src="https://github.com/user-attachments/assets/8a23961f-f1d4-4946-8ee8-d49389bc4483" />

While a CNN based approach follows such kind of architecture.
<img width="1536" height="177" alt="image" src="https://github.com/user-attachments/assets/e04ed33a-13f2-42b5-a9f8-d76c33a5038a" />

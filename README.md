# Automated Error Bar Detection-in Scientific Plots

## Generated Synthetic Dataset: https://drive.google.com/drive/folders/1_Fq-tS0AYp14ksZJqqLU6k33xmNR--v4?usp=sharing
## Sample Output (json): https://drive.google.com/drive/folders/1y1US00hwXvOTi4GI95sH_sYbPnfXTbx5?usp=sharing
## Sample Output Visualization: https://drive.google.com/drive/folders/1uQxoWutkwRfZiOOZKdN1ZlWVwyUOmU4I?usp=sharing



This project automates error bar detection in scientific plots using Procedural Generation and Vertical Intensity Profiling. It features a dataset of 3,000 images with high-fidelity JSON labels. The detection pipeline achieved an MAE of 21.98px across 112,000 data points in 23 minutes.

## Project Overview
The extraction of data from scientific visualizations is essential for large-scale meta-analysis. This project automates the identification of error bar extents starting from known data point coordinates. The system uses classical computer vision techniques to provide high-precision measurements, ensuring that statistical error margins are captured accurately from graphical representations.

## Technical Approach
The generation strategy utilizes procedural plotting to create a diverse dataset for validation. 

Diversity: Randomized line styles, colors, and markers simulate real-world scientific figures.
Ground Truth: Every plot is paired with a JSON annotation containing exact pixel coordinates for evaluation. 
Scale: The pipeline generated 3,001 unique images to ensure statistical significance during testing.

## Error Bar Detection Pipeline
The detection algorithm employs Vertical Intensity Profiling to measure the vertical extent of error bars. 

Preprocessing: Images are converted to grayscale and subjected to inverse binary thresholding to isolate graphical lines.
Directional Scanning: The algorithm scans upward and downward from the provided anchor points to identify line terminations.
Robustness: A 3-pixel horizontal search window is implemented to handle anti-aliasing and rendering artifacts.

## Evaluation Results

Metric	Result
Total Images Processed:	3,000

Mean Absolute Error (MAE):	21.9764 pixels

Accuracy (within 2.0px):	35.63%

Processing Speed	~2.10 iterations per second


The evaluation highlights the pipeline's effectiveness in clean environments while identifying grid lines and overlapping markers as primary sources of variance.

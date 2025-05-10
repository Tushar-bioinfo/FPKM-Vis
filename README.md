# FPKM-Normalization-and-Visualization
This project performs a comprehensive quality assessment of RNA-Seq data using FPKM (Fragments Per Kilobase of transcript per Million mapped reads) normalization, followed by multiple visualizations to evaluate biological replicates and assay consistency.

Input: Raw read count matrix (featureCounts) with gene lengths and four samples: vehicle_rep1, vehicle_rep2, drug_rep1, and drug_rep2.

FPKM Calculation: FPKM (Fragments Per Kilobase of transcript per Million mapped reads) values are calculated for each sample using the formula: FPKM = (read count × 10^9) / (gene length × total mapped reads). The results are saved for downstream analysis.

Scatter Plots: Log2-transformed FPKM scatter plots are generated to assess replicate concordance for vehicle_rep1 vs vehicle_rep2 and drug_rep1 vs drug_rep2. This helps evaluate the reproducibility across biological replicates.

Boxplots: Four boxplots are created to visualize the FPKM distributions for the vehicle and drug replicates. The plots show the log2(FPKM) values, with distinct color coding for vehicle (orange) and drug (purple) treatments.

Histograms: Histograms are generated for each sample, with fixed axis limits and uniform breaks. These plots visualize the distribution of log2(FPKM) values, providing insights into the data spread and shape.

Correlation Heatmap: A Pearson correlation matrix is computed between all four samples, with a heatmap visualizing the correlations. The heatmap uses a gradient color scale (white to orange) for clarity and ease of interpretation.

Tools Used: The analysis utilizes R base functions along with the ggplot2 and reshape2 packages for data visualization. Outputs are saved as PDF files for further review.

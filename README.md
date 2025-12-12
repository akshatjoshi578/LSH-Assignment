# LSH-Assignment
Duplicate Detection with MinHash LSH and MSMP+

This project implements a full pipeline for detecting duplicate Web products using MinHash-based Locality Sensitive Hashing (LSH) and a modified version of MSMP+, evaluated on a dataset of television products from multiple shops.

Pipeline Overview

Data Cleaning:
Normalises titles and attributes, extracts model words, removes high-frequency title stopwords, and standardises units (inch, hz).

MinHash & LSH:
Products are converted into sets of model words. MinHash signatures are generated and divided into bands to produce LSH candidate pairs at different thresholds.

MSMP+ Similarity:
Computation includes:

3-gram title similarity

Key–value structural similarity

Headword similarity for unmatched attributes
Combined into a hybrid score used for clustering.

Single-Linkage Clustering:
Candidate pairs are clustered using distance = 1 − similarity; all pairs in each cluster are predicted duplicates.

Bootstrap Evaluation:
Metrics (PC, PQ, F1*, F1) are computed on out-of-sample and averaged across multiple bootstraps.

Run Code file to obtain results used in paper

Output:
A table of PC, PQ, F1*, and F1 scores across LSH thresholds



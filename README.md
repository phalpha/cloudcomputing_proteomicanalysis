# Cloud Technologies for Proteomic Analysis of Adipogenesis

exploring the use of cloud computing on proteomic data for CS 273C, Cloud Computing for Biology and Healthcare

## Project Overview

This project evaluated the effectiveness of modern cloud technologies for conducting proteomic analysis, specifically focusing on temporal changes during adipogenesis (fat cell formation). We recreated visualizations from the paper "A spatiotemporal proteomic map of human adipogenesis" (Nature Metabolism, 2024) using Google Cloud Platform services.

## Research Context

Abnormal adipogenesis is linked to major metabolic diseases including obesity, cardiovascular disease, and diabetes - leading causes of global morbidity and mortality. Understanding the molecular changes during fat cell development through proteomics can reveal new biomarkers and therapeutic targets for precision medicine approaches.

## Technical Implementation

**Cloud Services Used:**
- Google Cloud Platform (GCP)
- BigQuery for data processing
- Vertex AI with Python Jupyter Notebooks
- Google Compute Engine VMs
- GATK HaplotypeCaller for pipeline benchmarking

**Analysis Pipeline:**
1. **Preprocessing**: Raw proteomic data processed through directDIA using Spectronaut
2. **Data Processing**: Import to BigQuery, cleanup and normalization with z-scores
3. **Analysis**: Hierarchical clustering and heatmap visualization of protein expression changes

### Scalability Performance
- Demonstrated effective weak scaling across 1-16 participants
- Runtime remained nearly constant (~511-557 seconds) as sample size increased
- **Cost per participant decreased significantly**: from $0.0308 (1 participant) to $0.0328 (16 participants)

### Security & Compliance
- Implemented HIPAA-compliant practices despite low PHI risk
- Used GCP's default encryption for data in transit and at rest
- Applied de-identification methods and data aggregation techniques
- Enabled audit logging for traceability

## Technical Achievements

Successfully replicated the temporal protein expression heatmap from the original Nature Metabolism paper, validating that cloud-based pipelines can effectively handle sophisticated proteomic analyses while providing built-in scalability and cost benefits compared to traditional local computing approaches.

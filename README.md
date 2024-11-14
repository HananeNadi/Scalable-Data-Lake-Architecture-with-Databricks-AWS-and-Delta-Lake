# Scalable-Data-Lake-Architecture-with-Databricks-AWS-and-Delta-Lake

## Overview

This project leverages Databricks, AWS, and Delta Lake to create a scalable data lake architecture for ingesting, processing, and analyzing Google Store data. This architecture follows a multi-layered approach (bronze, silver, and gold) to ensure data quality and make it ready for analytics and reporting.

## Architecture Components

### 1. **Data Ingestion**
   - Google Store data is ingested into AWS S3 as the primary storage layer.

### 2. **Lakehouse Layers**
   - **Bronze Layer**: Contains raw data in Delta format. No transformations are applied, so data is stored as ingested.
   - **Silver Layer**: Contains cleaned and standardized data. Here, transformations and cleaning are applied to ensure consistency.
   - **Gold Layer**: Contains business-level, aggregated data. This data is optimized for reporting and analysis, providing insights at an aggregate level.

### 3. **Data Processing with PySpark**
   - Data is processed using PySpark within Databricks. PySpark jobs manage the transition between layers, improving data quality at each stage.

### 4. **Data Consumption**
   - **Python**: Used to access processed data from S3 and connect it to Power BI for visualization and analysis.
   - **Power BI**: Visualizes data from the gold layer for business intelligence and reporting.

### 5. **Data Quality Improvement**
   - Data quality improves progressively as it moves from the bronze to the gold layer through cleaning, transformation, and aggregation.

## Data Pipeline
![ec](https://github.com/user-attachments/assets/91e0be2d-c8e9-406a-847b-a48d15e8b588)

## Getting Started
### Prerequisites
- **AWS Account:** Required for S3 storage.
- **Databricks Account:** Required to run PySpark jobs and manage the data lake.
- **Power BI:** Required for visualizing the gold layer data.
- **Python:** For additional data processing and analysis, and for connecting Power BI to S3.

## Visualisation 
![dashboard](https://github.com/user-attachments/assets/06945c41-0b36-44bb-9b05-6f7773dcd1d5)

## Future Improvements
- **Automate ETL Pipelines:** Schedule jobs for automated data ingestion and transformation.
- **Expand Data Sources:** Integrate additional data sources into the data lake.
- **Enhance Reporting:** Explore advanced visualizations and dashboards in Power BI for more in-depth insights.

## Conclusion

This data lake architecture demonstrates a scalable and flexible solution for handling large datasets with varying levels of transformation and aggregation. By leveraging Databricks and Delta Lake on AWS S3, the architecture provides a structured, multi-layered approach to data management, enabling efficient ingestion, processing, and storage. The bronze, silver, and gold layers facilitate data quality improvements and ensure that only cleaned and aggregated data is available for business reporting.

Using Python to connect Power BI with the data stored in S3 further enhances the usability of this architecture by making data accessible for real-time visualization and analysis. This integration enables business users to gain insights, make data-driven decisions, and develop a deeper understanding of business metrics.

This architecture is also adaptable for future enhancements, such as automation, additional data sources, and more sophisticated reporting capabilities. Overall, this project provides a solid foundation for a modern data lake that can grow with your data and analytical needs.


## Authors

- [@HananeNadi](https://github.com/HananeNadi)

## Contact Me

Feel free to contact me at:

- Email: nadi.hanane01@gmail.com
- LinkedIn: [Hanane Nadi](https://www.linkedin.com/in/hanane-nadi-32089a251/)

## Kibana and Elasticsearch Dashboard
This project involves building a Kibana dashboard using Elasticsearch (version 8.1.0) on a Windows system to analyze and visualize the Superstore Sales dataset.
### Prerequisites
Before getting started, ensure you have the following software installed:
- Elasticsearch 8.1.0
- Kibana 8.1.0
Both Elasticsearch and Kibana can be downloaded from the official Elastic Downloads page.
### Setup Instructions
1. **Download and Extract Elasticsearch and Kibana**
  - Download Elasticsearch and Kibana (version 8.1.0) from Elastic Downloads.
  - Extract the downloaded files to appropriate locations on your system (e.g., C:\Program Files\).
2. **Add Bin Paths to Environment Variables**
  - Add the bin directories for both Elasticsearch and Kibana to your system's environment variables:
    + Elasticsearch bin path: C:\Program Files\elasticsearch-8.1.0\bin
    + Kibana bin path: C:\Program Files\kibana-8.1.0\bin
3. **Start Elasticsearch**
  - Run elasticsearcg.bat file in command prompt as administrator.
  - Note: During the first run, Elasticsearch will generate a password for the elastic user. Make sure to note down this password, as it will be required for accessing both Elasticsearch and Kibana.
4. **Start and Login Into Kibana**
  - Run kibana.bat file in another command prompt window as administrator.
  - Once Kibana is running, open your browser and go to http://localhost:5601.
  - Log in using the elastic user credentials and the password you noted earlier.
  - If this is the first time you’re accessing Kibana, you’ll need to use the enrollment token to authenticate.
### Upload Dataset
- For this project, we used the Superstore Sales dataset from Kaggle. You can download the dataset here: https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting?resource=download
- Once downloaded, upload the dataset into Kibana using the Upload File option.
- Elasticsearch will analyze and index the dataset, creating a new index pattern (referred to as a Data View in Kibana). You can view and manage the index pattern in Management > Stack Management > Index Patterns.
### Explore the Data
- Using Dev Tools in Kibana, run queries to explore and analyze the data. You can access the Dev Tools Console in Kibana under Management > Dev Tools.
### Create Scripted Fields
- If you need additional analysis, you can create scripted fields for your data. To create a scripted field:
  1. Go to Management > Stack Management > Data Views.
  2. Select the Data View you created.
  3. Click on Scripted Fields and create any necessary scripted fields for your analysis.
### Create Visualizations and Dashboard
- Use the Visualize Library to create various visualizations based on your queries and insights.
- Add your visualizations to a Kibana Dashboard to combine them in a single view.
### Conclusion
This project demonstrates how to use Kibana and Elasticsearch to upload a dataset, explore it using queries, create visualizations, and build a dashboard for data analysis.

Feel free to explore further and experiment with other visualizations and analyses as needed.

**Streaming Real-Time Stock Data with Python and Kafka**

In today’s fast-paced financial markets, having access to real-time stock data is crucial for traders, analysts, and investors. Streaming this data efficiently and reliably can be challenging. However, with the power of Python and Apache Kafka, you can easily set up a data streaming pipeline to capture, process, and analyze real-time stock data.

**Why Use Kafka for Real-Time Data?**

Apache Kafka is a distributed streaming platform for building real-time data pipelines. 
It offers several advantages for streaming real-time stock data:

Scalability: Kafka can handle massive amounts of data and scale horizontally to meet growing demands.

Durability: Kafka retains data for a specified period, making it suitable for historical analysis.

Reliability: It ensures data integrity, even in hardware failures or network issues.

Publish-Subscribe Model: Kafka’s pub-sub architecture allows multiple consumers to subscribe to real-time data streams simultaneously.

**Project Overview**

This project demonstrates the implementation of a real-time data pipeline for stock price analysis using Confluent Kafka, Databricks, PySpark, and Delta Lake. It ingests live or simulated stock price data via Kafka, processes it using Databricks, calculates key stock metrics (like moving averages and volatility), and provides real-time alerts. The processed data is stored in Delta tables for easy querying, with an interactive dashboard for visualizing stock trends and metrics.

**Technologies Used**

Confluent Kafka: For real-time data streaming and message delivery.

Databricks: For big data processing and analytics using PySpark.

Delta Lake: For real-time and batch data storage.

Apache Kafka Producer & Consumer: For producing and consuming stock price data.

PySpark: For processing the data and calculating metrics.

Databricks Notebooks: For visualizing the data and creating dashboards.

**Features**

Real-Time Stock Price Streaming: Stream live or simulated stock data using Kafka.

Data Processing & Analysis: Calculate real-time metrics such as moving averages, volatility, and price changes.

Alerts: Trigger alerts for significant stock price fluctuations (e.g., > 1% change).

Interactive Dashboard: Visualize stock trends and key metrics in real-time using Databricks.

Delta Tables: Store real-time and batch data for efficient querying and analysis.

Stock Symbol Filtering: Filter stock data by symbol (e.g., MSFT, AMZN, AAPL, GOOG).

Daily Summary Metrics: Display average closing prices and total volumes per day.

**System Architecture:**

Kafka Producer: Generates synthetic stock price data and sends it to a Kafka topic.

Kafka Consumer: Reads data from Kafka, processes it with PySpark, and writes the results to a Delta table.

Databricks: Uses PySpark to process and analyze the stock data, including calculating moving averages, volatility, and price changes.

Dashboard: Displays visualizations such as bar charts, pie charts, and time series graphs for real-time stock analysis.

**Setup & Installation**

1. Kafka Setup: You need to have Apache Kafka and Confluent running to simulate the real-time data streaming.

2. Install Dependencies: To run the project locally or in a Databricks notebook, install the following Python libraries:_ pip install confluent-kafka pyspark_

3. Run the Producer Script The Kafka producer generates stock price data and sends it to the Kafka topic (stocks_analysis)._ python producer.py_

4. Run the Consumer Script: The Kafka consumer reads the data, processes it with PySpark, and writes the results to Delta tables. _python consumer.py_

5. Databricks SetupUpload your notebooks to Databricks for visualization and interactive analysis. Use the Delta Lake format to store and query your processed stock data.

6. Dashboard: Once data is processed, use Databricks to visualize stock trends using various charts and tables, including Bar charts for trading volume., Line charts for stock prices over time., Scatter plots for volatility and moving averages.

![image](https://github.com/user-attachments/assets/ceb6c155-fe00-4fbd-b7e5-db25bb01914e)

**Insights**

● Bar Chart (Top Left): Shows the total trading volume for stocks (AAPL, AMZN, GOOG, MSFT), identifying the most actively traded stock.

● Pie Chart (Top Right): Displays the percentage contribution of each stock to overall volatility.

● Line Chart (Middle Left): Compares maximum moving averages (price trends) and maximum volatilities for stocks.

● Scatter Plot (Bottom Left): Correlates volatility with moving averages to analyse stock price stability and trends.

● Summary Table (Middle Right): Provides key metrics like average closing price for each stock by date.

● Window Data Table (Bottom Right): Shows real-time streaming batches with processing windows and metrics.

● Raw Data Table (Bottom Right Corner): Displays unprocessed stock data like Open, High, and Volume for analysis.


**Example Output**

Real-Time Stock Price Chart: A live feed showing stock prices as they change in real-time.

Moving Average Plot: A line chart of stock price moving averages over time.

Alerts: Notifications when stock price changes exceed a threshold (e.g., 1%).

Summary Table: Daily summary of stock metrics (e.g., average price, total volume).

**Contributors**

- Bharat Dhungana
- Satish Koirala
- Bikash Thapa Magar
- Samir Bhattarai
- Aravind 

This project is licensed under the MIT License - see the LICENSE file for details.

**Future Work**

Extend the project to support more stock symbols.

Implement machine learning models for stock price prediction.

Enhance alert systems with more complex triggers and notifications.

Optimize the real-time pipeline for better performance and scalability.




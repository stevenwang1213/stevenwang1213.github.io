## Sz-Je Wang 10K sentiments analysis

**Project description:** 
This project aims to analyze the sentiment of 10-K filings from S&P 500 companies using ML and LM dictionaries for positive and negative words. It calculates the sentiment score for each company's 10-K filing and generates an output with the sentiment scores.

### 1. Summary

In this study, I aimed to investigate whether the sentiment in 10-K filings contains value-relevant information related to stock returns, with a particular focus on environmental, social, and governance (ESG) issues. I compiled a sample of 10-K filings of S&P 500 companies spanning various firms and industries. I extracted sentiment measures from the filings using two different sentiment dictionaries, the LM and ML dictionaries and created "contextual sentiment" measures by identifying the sentiment of ESG-related topics discussed in the filings. My findings suggest a relationship between sentiment scores and stock returns, with positive sentiment related to ESG issues being associated with higher returns, while negative sentiment related to ESG issues not showing a significant relationship with returns. The contextual sentiment measures also provide insights into the relationship between ESG sentiment and stock performance, highlighting the potential importance of textual analysis in predicting stock performance.

In the file folder, I have three subfolders: Building Sample, Exploration, and Report. In the Building Sample folder, I create the code for sentiment analysis and compile the data. Next, I use this data to generate graphs in the Exploration folder. Finally, I write the Report based on these analyses. Additionally, I have created an Analysis Sample that combines the S&P 500 stock returns with sentiment scores for each company. To conclude my study, I compare the sentiment scores across different sectors and calculate the mean to determine which sector performs the best and how their performance is related to their sentiment scores.

### 2. Data section

#### Sentiment Variables
The sample comprises 10-K filings from companies listed in the S&P500 index, sourced from the SEC's EDGAR database. To obtain the data, I downloaded the text files and processed them to generate a CSV file by the download text code, which was then saved to my local machine.

#### Sentiment Variables
I first combined the list of negative words from the ML and LM dictionaries to create a set of negative words. The sentiment score was calculated by dividing the number of negative words present in the cleaned text of a 10-K filing by the total number of words in the text. This produced a fraction representing the proportion of negative words in the document. Other than that, I also create my own positive and negative words list to run the sentiment score analysis.

The selection of topics for contextual sentiment measures was based on their potential impact on stock performance and the company's perception in the market. These topics were carefully chosen to represent key areas of interest for investors and analysts, such as financial performance, management outlook, and industry trends. By focusing on these specific areas, I aimed to capture the nuances in sentiment that could directly influence stock prices and market sentiment. To provide a comprehensive overview of my final analysis sample, I presented summary statistics, including central tendency and dispersion measures for each variable. These statistics offer valuable insights into the distribution and characteristics of the data, helping to set the stage for my analysis. Furthermore, I conducted basic smell tests to ensure the validity of my sentiment measures. These tests included checking for variation in the measures, ensuring that industries typically associated with positive or negative sentiment were accurately represented, and confirming that no major anomalies were present in the data. By performing these tests, I aimed to establish a solid foundation for my analysis, enhancing the reliability and interpretability of my findings.

### 3. Analysis and Result

The relationship between return variables and LM sentiment variables showed different patterns compared to ML sentiment variables. The differences in signs and magnitudes could be attributed to the varying methodologies used in sentiment analysis.

As part of the coding process, I intend to analyze the relationship between the returned variable and two "LM Sentiment" variables (positive and negative), and the relationship between the returned variable and two "ML Sentiment" variables (positive and negative). I will examine the sign and size patterns of these correlations to gain insight into the relationship between the variables. Then discuss why sentiment in those contexts might be value relevant to stock performance. This could include how the specific context affects investor perception or how it might influence the company's future performance. At the end I want to test differences in the sign and magnitude of relationships between sentiment measures and return variables. Speculate on potential reasons for these differences, which may include changes in the importance of specific sentiment indicators or the influence of external factors on the relationship.

### 4. Conclusion
The positive or negative sentiment score can have a significant impact on a stock's return. If the negative sentiment score is higher than the positive score, it may indicate that the company's future growth prospects are not favorable. Consequently, the stock return is likely to decrease or be lower compared to other stocks in the same sector.

As the result,I beleive that investor sentiment has been widely acknowledged as a factor that can cause fluctuations in stock prices, including sudden market shocks and even short-term jumps. As a result, sentiment indicators have become an important tool for applied analysis. However, since investor sentiment cannot be directly observed, constructing accurate sentiment indicators has been a topic of great interest among scholars.

Jinsong Zhen's Contribution to the Project:
* Web-scraped financial data from news sources, including MarketWatch, Benzinga, and Motley Fool: https://colab.research.google.com/drive/1-TJHscwdce7vYyVaMmMex4PDT4t2b8rM
* Conducted Sentiment Analysis on the articles news of 90 company public stocks with the most postiive sentiments: https://colab.research.google.com/drive/1Iqf-ha5MYygdND6tMRDY7J7dXpNcFyAO?usp=sharing
* Built a tool to generate quiz score: https://colab.research.google.com/drive/1xoEN47CsaV1sonplE6VJs379ScXyFvcF

FinSight: Your Vision for Financial Insights

FinSight is a web based portfolio balancer that uses NLP and sentiment analysis to analyze 10K and 10Q Fiscal Reports to generate an optimal master list of securities for trading. Then, that list is filtered through a risk assessment quiz that the user completes to understand the risk profile. Finally, that filtered list of securities is balanced into an investible portfolio using portfolio balancing techniques.

A Dashboard Example: https://public.tableau.com/app/profile/lakshmi.gadepalli/viz/ProjectViz_16819376507930/Dashboard1

Risk Aversion Survey: https://public.tableau.com/app/profile/lakshmi.gadepalli/viz/ProjectViz_16819376507930/UserSurvey

Academic Report & Poster:
</pre>
DOC:
1. Final report: https://github.com/jzhen3/Financial-Investment-Recommender/blob/main/DOC/team075report.pdf
2. Final poster: https://github.com/jzhen3/Financial-Investment-Recommender/blob/main/DOC/team075poster.pdf
</pre>

If you want to setup our Tableau locally, you can do the following:

How to setup and run:
1. Clone Repository

2. Open Tableau Project file: Project Viz.twbx found in CODE folder

3. From the data_sources folder in the repository, do the following:
<pre>
  a. Add newEval.csv and dva_stock_prices_u.csv as data source dependencies to "sentiment_stocks" data source in Tableau 
</pre>

4. Setup Jupytab by doing the following:
<pre>
  a. Install conda and create a virtual environment with Python=3.7
  b. Install Jupyter Kernel Gateway following these instructions: https://github.com/jupyter-server/kernel_gateway
  c. Install JupyTab following these instructions here: https://github.com/CFMTech/Jupytab#installation
  d. We have provided the config.ini and tester.ipynb (portfolio balancer code) in the repository
  e. Using your terminal, navigate to the config.ini file directory
  d. Then run: jupytab --config=config.ini
  e. Once the jupytab server is started, you will get a link in the terminal that looks like (please open): http://sangeetas-mbp.lan:8888 to verify that your Jupytab instance is live

5. Launch dashboard and leverage Jupytab output as a Web Data Source. Do this by:
  a. Open Tableau Data Sources and add a new Web Data Connector data source with the link generated above
  b. Take the quiz and proceed to data visualization to evaluate the dashboard
  c. If you notice that the data does not update, refresh the data sources. This is a known Tableau limitation where WDC does not support live connection and only allows extracts.
  d. Feel free to preview the data table and hit refresh to bring in the data

6. Your Tableau Dashboard and Visualization is ready for exploration!
</pre>


CODE:
<pre>
  Visualization Data: A python notebook that generates dva_stock_prices_u.csv output that is used in Tableau Input
  Sentiment Analysis: A python notebook that calculates the positive, negative or neutral sentiment scores for headlines
  Documents: Misc. documents
  data_sources: Data source dependencies for Tableau (Project Viz.twbx)
</pre>

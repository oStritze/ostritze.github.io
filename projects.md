---
layout: default
title: Projects
permalink: /projects/
images:
  - /static/figs/ma/general_1.png
  - /static/figs/ma/general_2_2.png
  - /static/figs/ma/medical_2.png
  - /static/figs/ma/input_mask_full_example.png
  - /static/figs/ma/model_comparison_blur_adapthist_clip01.png
  - /static/figs/ma/ModelEval.drawio.png

---

# Projects

A (chronological) excerpt of projects i was working on.

<br>

---

<br>
## 2025
### Recommender System for Medical Treatment Planning 
- __Context:__ Funded Research Project - [iPAB](https://www.scs.fraunhofer.de/de/referenzen/iPAB.html)
- __What:__ Development of a Recommender System for inpatient care, in cooperation with a regional software delevoper and two hospitals. The goal was to reduce time spent on individual treatment plan generation, which legally is to be done by qualified nurses. Worked on data preprocessing of 40.000 patient visits, creating a usable dataset from JSON payloads (DVC, Polars, Pandas) which was feasible for training a model based on documented care items in different hostpitals with different data structures, including data versioning. Designing Baseline models (Decision Trees, Logistic Regression), complex models (AutoEncoders, MLP) and explainable Models to show health pracitioners high influence features (Explainable Boosting Machines). Models had to deal with highly unbalanced labels. Programming a usable demo (SOAP). Design of a vignette study to test models efficiency as well as supervising a Master Thesis in that context.  
- __Results:__ Some results are going to be published in the foreseeable future - check [orcid](https://orcid.org/0000-0003-1772-7428). The assistant that was evaluated was able to reduce the time spent planning by 2.3 minutes per planning. 
- __Tech used:__ DVC, Bash, MSSQL, Docker, Poetry, Polars, Explainable Boosting Machines, Torch, scikit-learn, Gitlab-CI, spyne (SOAP)


## 2024
### Quality Outcome Prediction of Gear Boxes for electric vehicles
- __Context:__ Industry Project (for Fraunhofer IIS)
- __What:__ Quality and throughput time prediction for gear-box production process. Data preprocessing of process data, feature engineering (tf/idf, n-grams), modeling and training of Trace-Representation models to predict the quality of ongoing production processes. Visualization of processes.
- __Results:__ Customer gained insights into their complex production processes via their data (transparency) and understood that eliminating exisint data quality issues (missing naming conventions) may improve results furthermore.
- __Tech used:__ Docker, Kubernetes, DVC, Poetry, MLFlow, Torch, NLP (tf-idf, n-gram), pm4py

## 2023
### AI-Assistant for intralogistic Material Delivery Planning 
- __Context:__ Industry Project (for Fraunhofer IIS)
- __What:__ Automating material delivery method planning for assembly lines in engine manufacturing by training a ML model. Creating automated ETL data pipeline from customers cloud infrastructure to get daily data from ERP systems. Data preprocessing, feature engineering and training of a multi-class unbalanced classification (Random Forest, CatBoost, Logistic Regression) of delivery strategies based on target positions in manufacturing as well as material features (size, weight). Development of a usable demo for the customer (Streamlit). Support for in-line integration of customers IT.
- __Results:__ CatBoost models were robust and quite well performing as most features were categorical. Models were ported to production systems by the companies IT later on to be integrated in their planning system. 
- __Tech used:__ Docker, Kubernetes, sftp, bash/cron, conda, scikit-learn, Catboost, imbalanced-learn, pandas, streamlit


## 2022
### Multivariate Machine Learning - Predicting and communicating outcome of COVID-19 hospitalizations with medical images and clinical data
- __Context:__ Master Thesis
- __Abstract:__ We propose a visual analytics framework to support the prediction, analysis, and communication of COVID-19 hospitalization outcomes. Although several real-world data sets about COVID-19 are openly available, most of the current research focuses on the detection of the disease through chest X-ray images. Until now, no previous work exists on combining insights from medical image data with knowledge extracted from clinical data, predicting the likelihood of an intensive care unit (ICU) visit, ventilation, or decease. Moreover, available literature has not yet focused on communicating such results to the broader society. To support the prediction, analysis, and communication of the outcomes of COVID-19 hospitalizations on the basis of a publicly available data set comprising both electronic health data and medical image data, we conduct the following three steps: (1) automated segmentation of the available X-ray images and processing of clinical data, (2) development of a model for the prediction of disease outcomes and a comparison to state-of-the-art prediction scores for both data sources, i.e., medical images and clinical data, and (3) the communication of outcomes to three different user groups (namely, medical and clinical experts, experts in data analytics, and the general population) through an interactive dashboard. The dashboard is designed to enable users to solve user-specific tasks, also defined in this work. Preliminary results indicate that the prediction results are improved by combining medical image data with clinical data, while analysis and communication of hospitalization outcomes prove to be a wide and significant topic in the context of COVID-19 prevention.
- __Results:__ The full thesis is available [here](https://repositum.tuwien.at/handle/20.500.12708/80544) and [here](static/thesis-stritzel-paco.pdf). Parts of the thesis have been published as a paper [here](https://diglib.eg.org/items/bd4e914f-6dc5-4367-a82a-6c955085b7a7)
- __Tech used:__ pandas, opencv, pytorch, nvidia cuda, scikit-learn (unbalanced multi-target prediction and clustering), streamlit, plotly, 

<div class="swiper">
  <div class="swiper-wrapper">
    <!-- Slides -->
    {% for image in page.images %}
      <div class="swiper-slide">
        <img src="{{ image }}" alt="Slide {{ forloop.index }}">
      </div>
    {% endfor %}  </div>

  <!-- Pagination and Navigation -->
  <div class="swiper-pagination"></div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
</div>
<br>


### History of Twitter - How Tweets are disappearing over time
- __Context:__ Interdisciplinary Project in Master Curriculum
- __What:__ Twitter is used a lot in social sciences and communities to identify trends, political discussions and even in catastrophies to communicate and share information. While a lot of research was conducted in that regard, less is focused on how tweets are disappearing over time. This work provides an overview of causes of tweets disappearing, how to measure it, where to get historical twitter data and what are possible causes for tweets disappearing (gender, text, sentiment, language). 
- __Results:__ This work shows that language has a high influence over the tweet disappearance and that it is non-trivial to infer language from outside of twitter, it is non-trivial to work with a high amount of twitter data and we provide an overview of most used terms for deleted or privated tweets of male and female users of Twiter which shows clear differences. Parts of this work have been published [here](https://ojs.aaai.org/index.php/ICWSM/article/view/22182).
- __Tech used:__ hadoop, spark, REST, pandas, scikit-learn, NLP (tf-idf, n-gram), bootstrapping / data sampling

![Disappearence of tweets over time](/static/figs/ds/tweetskb_available_vs_unavailable_bigger.png)


## 2018
### Designing a Centralized Logging Platform
- __Context:__ Internal Project @ ING-DiBa
- __What:__ Design and development of an on-premise, multi-tenant monitoring and log aggregation platform, based on Redhat OpenShift/Kubernetes, Docker, Apache Kafka and Elastic-Stack: Elasticsearch, Kibana, Logstash and Beats. Handling terabytes of daily log data from hundreds of application servers Kafka. Automation with Ansible, Build and Deployment with Jenkins. After go-live, maintenance and onboarding as well as first-level support for internal customers. Knowledge transfer and mentoring of new employees and apprentices as well as close cooperation with international development teams and architects of holdings company ING.
- __Results:__ A plethora of smaller Elasticsearch clusters, tuned to fullfil different search duties for developers in different development stages (load testing, production, development of microservices). 
- __Tech used:__ Docker, Kubernetes, Openshift, Jenkins, Ansible, Elasticsearch, Logstash, Kibana, Kafka, mTLS


## 2016
### Bachelor Thesis - Comparing Apache Flink and Apache Spark for real-time Fraud Detection
- __Context:__ Bachelor Thesis @ ING-DiBa 
- __What:__ Scams and Fraud are a huge problem for financial institutes as they often balance a fraction or the whole amount of lost money, depending on the case. Having a real-time sytem that alerts and stops transactions in place which may be deemed fraudulent is thus a reasonable idea. The input data was log files from online banking servers. Due to the load distributions, the target system needed to be able to cache a specific amount of log data (for a specific session duration) for all logged in customers in real-time, and if suspicious activities took place, alert it. There was ongoing work in parallel so the experiences and insights were to be integrated at some point into production systems, therefore there was a lot of architectural work to be done: so for example the system had to communicate with different systems like Apache Kafka to read and write data, and be able to do that securely with mTLS.
- __Results:__ To compare the two systems, a benchmark was done. After implementing a ruleset that was proven to identify fraudulent cases on a real example logfile and implementing the windowing functionality in Spark and Flink, a four-node Hadoop cluster with YARN was set up to host Spark and Flink. Both Frameworks were provided the logfile via a single-node Kafka machine and business (f.i. exactly-once processing) and technical metrics (ram usage, cpu usage, ...) were reported. Both Frameworks were able to solve the task, with Flinks windowing behaving more natural. 


## 2015
### Developing a Letter Forecast
- __Context:__ Internship @ING-Diba 
- __What:__ In order to optimize ressources and plan personell for high demands, the goal was to develop a forecast for letter dispatch demands. The letters were printed and enveloped on site so the first two weeks i joined the team to "gather domain knowledge". After lots of data analysis and following this neat [book](https://otexts.com/fpp3/), different forecasting models were chosen and compared. Due to the amount of different types of letters being produced and sent to customers, the letters were hierarchically clustered into different groups, outliers were removed. Initially the goal was to produce hourly forecasts but this seemed to fine to achieve, so in the beginning a weekly (keeping in mind seasonality) prediction was made. The weekly prediction was then distributed on the weeks working days (keeping in mind holidays and special days), with another seasonality in place. A Holt-Winter seasonal decomposition forecast was giving a robust forecast over a short trial phase. 
- __Results:__ The target user-group worked in Microsoft Excel and so the resulting tool was best brought to them via excel. Therefore, the R code and plain math formulas were ported to VBA to established a nightly ETL data pipeline, enabling daily forecasts. 

### 3D-Printing Tactile Maps for blind and visually impaired individuals

- __Context:__ Interdisciplinary Project
- __What:__ Accessible 3D printers are a good way of creating maps for blind and visually impaired individuals. In this project we tried out two different printing techniques - FDM and SLA - and conducted a study at a school for visually impaired children in Nuremberg to test error rates, haptics and usability of city maps. We used a vignette study of 2 groups and checked signifiance via t-tests. 
- __Results:__ Despite being way more expensive and looking way cleaner, SLA did not yield better results and participants were liking the more "rough" FDM maps better as the printing artifacts made the edges and objects better to distinguish.
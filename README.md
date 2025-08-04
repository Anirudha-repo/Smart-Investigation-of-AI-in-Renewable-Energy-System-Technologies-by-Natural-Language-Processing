# Smart Investigation of AI in Renewable Energy Systems

This repository contains the code and resources for a final year project that uses Natural Language Processing (NLP) to analyze trends in Artificial Intelligence (AI) applications within the renewable energy sector. The project is based on the methodology of a key research paper and explores two different topic modeling approaches for a comprehensive analysis.

## Project Resources

This repository includes the following files and assets for a complete and reproducible analysis:

  - `AI in Renwable energies.csv`: The dataset used for the analysis, containing over 5,000 research abstracts from the Scopus database.
  - `Scopus Search Engine.ipynb`: The Jupyter Notebook containing the code used to collect the dataset from the Scopus database.
  - `Renewable energy.pdf`: The research paper that serves as the methodological foundation for this project.
  - `Project Methodology`: A visual representation of the methodology followed, extracted from the referenced research paper.

## Methodology

The project follows a systematic approach to uncover patterns in research literature. The core steps, as outlined in the attached methodology image, are:

1.  **Data Collection:** Raw textual data (titles and abstracts) was collected from the Scopus database.
2.  **Data Pre-processing:** The text was cleaned by removing stopwords, punctuation, and performing advanced techniques like lemmatization.
3.  **Data Analysis:** Two distinct topic modeling algorithms, LDA and BERTopic, were used to identify the underlying themes.
4.  **Results and Discussion:** The identified topics were analyzed, visualized, and discussed to highlight key trends for decision-makers.

## Implementation Details

The project is implemented in two separate Jupyter Notebooks, each exploring a different topic modeling approach. This allows for a comparison of results between a classical and a modern NLP technique.

### 1\. Analysis using LDA Algorithm

  - **Notebook:** `Analysis_using_LDA.ipynb`
  - **Algorithm:** Latent Dirichlet Allocation (LDA)
  - **Purpose:** This notebook implements a classical topic modeling approach using `scikit-learn`'s `LatentDirichletAllocation`. It serves as a robust baseline for the analysis.
  - **Key Steps:**
      - Data pre-processing with lemmatization.
      - Conversion of text into a document-term matrix using `CountVectorizer`.
      - Training the LDA model to identify 10 core topics.
      - Visualization of topic distribution and topic trends over time using `matplotlib` and `seaborn`.
  - **Outcome:** Provides a clear understanding of the major research topics and their evolution based on word co-occurrence.

### 2\. Analysis using BERTopic

  - **Notebook:** `Analysis_using_BERTopic.ipynb`
  - **Algorithm:** BERTopic (leveraging BERT, UMAP, hDBSCAN, and c-TF-IDF)
  - **Purpose:** This notebook implements a more advanced and modern topic modeling approach that leverages a pre-trained language model (BERT) to find semantically relevant topics.
  - **Key Steps:**
      - Installation of the BERTopic library and its dependencies (`tf-keras`).
      - Data pre-processing optimized for BERTopic's internal mechanisms.
      - Training the BERTopic model to automatically discover topics.
      - Manual analysis of top words to merge topics into broader "metatopics."
      - Custom visualization of metatopic distribution and trends over time using `matplotlib` and `seaborn` to ensure stability against API changes.
  - **Outcome:** Offers a more nuanced and potentially higher-quality set of topics compared to the LDA model, based on semantic similarity.

## Getting Started

To run the notebooks, ensure you have the necessary libraries installed. It is highly recommended to set up a dedicated virtual environment for each notebook to manage dependencies properly.

For the **LDA notebook**, install the following:

```sh
pip install pandas scikit-learn seaborn matplotlib nltk
```

For the **BERTopic notebook**, create a separate environment and install:

```sh
pip install pandas bertopic tf-keras
```

Then, open either notebook in Jupyter or Google Colab and run the cells sequentially to reproduce the analysis.

## Key Findings
### Using LDA Algorithm
- The LDA analysis revealed four major metatopics, providing a clear overview of the research landscape. The key findings from this analysis are:

**1. Most Prominent Research Areas:**
* **"Smart Grid & Energy Management"** and **"AI Models and Optimization"** emerged as the two most dominant areas of research, as shown by the topic distribution plot. This indicates a strong focus on both the application of AI for managing energy systems and the development of the underlying algorithms themselves.

**2. Evolving AI Trends:**
* The **"RE Forecasting and Prediction"** metatopic showed a consistent and accelerating upward trend over the years, signifying a growing focus on using AI to predict renewable energy generation.
* Research within the **"Smart Grid & Energy Management"** metatopic also demonstrated a steady increase, highlighting the continuous effort to apply AI for optimizing grid operations and managing new technologies like electric vehicles.

**3. Gaining Traction in Specific Technologies:**
* The analysis identified a clear shift towards more advanced AI techniques, with the **"AI Models and Optimization"** metatopic (which includes terms like "deep learning," "neural network," and "optimization") showing a noticeable rise, particularly in recent years. This suggests that the research community is moving beyond traditional methods to more sophisticated AI solutions.

In conclusion, the LDA model provides a clear picture of a dynamic research field where the application of AI for forecasting and smart grid management is expanding rapidly, driven by the increasing use of advanced deep learning and optimization techniques.

### Using BERTopic

- Solar Energy Systems emerged as the most dominant research focus, highlighting strong interest in photovoltaic optimization and solar forecasting.
- AI & Deep Learning models (e.g., CNNs, LSTM, ANN) are increasingly being applied for intelligent energy management and demand prediction.
- Wind Power Forecasting & Grid Integration remains a major theme, emphasizing the need for real-time predictions and seamless power distribution.
- A noticeable surge in AI-driven renewable energy publications since 2018 reflects growing adoption of smart technologies in sustainability research.
- Research is shifting from basic ML models to advanced optimization strategies and policy-aware AI systems, offering decision-makers actionable roadmaps for energy innovation.

## References
  - The methodology for this project is inspired by the research paper: "Smart investigation of artificial intelligence in renewable energy system technologies by natural language processing: Insightful pattern for decision-makers."
  - Data was collected from the Scopus database using the provided search engine code.

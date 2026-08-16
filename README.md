# ColabWorks

A practical collection of Google Colab and Jupyter notebooks covering business analytics, exploratory data analysis, machine learning, natural language processing, OCR, and AI-assisted knowledge extraction.

The repository is intended for learning, experimentation, and adapting individual workflows to new datasets. Each notebook can be opened directly in Google Colab; any external files, services, or source projects it needs are identified below.

## Notebook catalogue

| Notebook | Focus | Main techniques | Data or service required | Open in Colab |
|---|---|---|---|---|
| [Bike Sharing](./BizAnalytics_W01_Bike_Sharing.ipynb) | Predict bike-rental demand | Descriptive analysis, outlier handling, correlation analysis, regression, random forest, feature importance | Bike-sharing CSV downloaded by the notebook | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/BizAnalytics_W01_Bike_Sharing.ipynb) |
| [Reuters Authorship](./BizAnalytics_W02_Reuters_Authorship.ipynb) | NLP and text mining using Reuters articles | Cleaning, tokenisation, lemmatisation, TF-IDF, Word2Vec, Naive Bayes, SVM, LDA | Reuters C50 dataset downloaded by the notebook | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/BizAnalytics_W02_Reuters_Authorship.ipynb) |
| [Customer Segmentation](./BizAnalysis_W04_Customer_Segmentation.ipynb) | Segment e-commerce customers and predict customer categories | Data preparation, product and customer clustering, PCA, SVM, ensemble classifiers | E-commerce CSV downloaded by the notebook | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/BizAnalysis_W04_Customer_Segmentation.ipynb) |
| [Demand Forecasting](./BizAnalysis_Demand_Forecasting.ipynb) | Forecast store-item sales | Time-series preparation, scaling, LSTM, 1D convolution, prediction visualisation | Train and test CSVs downloaded by the notebook | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/BizAnalysis_Demand_Forecasting.ipynb) |
| [Airbnb Booking EDA](./MLSeries_AirBnB_Booking_Analysis_using_EDA.ipynb) | Explore Airbnb listing data | Data cleaning, missing-value treatment, descriptive statistics, distributions, count plots, time trends | `sample_data/Airbnb_Open_Data.csv` | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/MLSeries_AirBnB_Booking_Analysis_using_EDA.ipynb) |
| [Zomato Data Analysis](./MLSeries_Zomato_Data_Analysis_Using_Python.ipynb) | Analyse restaurant types, ratings, costs, votes, and online ordering | Data preparation, aggregation, count plots, box plots, heatmaps | `sample_data/Zomato-data-.csv` | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/MLSeries_Zomato_Data_Analysis_Using_Python.ipynb) |
| [Groq OCR](./20260617_ColabWorks!_Groq_OCR.ipynb) | Extract structured invoice information from an image | Base64 image encoding and multimodal LLM extraction | `Invoice.jpg` and a Groq API key | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/20260617_ColabWorks%21_Groq_OCR.ipynb) |
| [Dynamic Schema Knowledge Extraction](./ColabWorks!_Knowledge_Extraction_Using_Dynamic_Schema_Generation.ipynb) | Generate a schema from business requirements and extract structured data from a PDF | Dynamic schemas, vision parsing, contextual PDF extraction | Source project, `input/PO.pdf`, and OpenAI or Azure OpenAI configuration | [Launch](https://colab.research.google.com/github/gitguy007/2026-ColabWorks/blob/main/ColabWorks%21_Knowledge_Extraction_Using_Dynamic_Schema_Generation.ipynb) |

## Quick start with Google Colab

1. Select a **Launch** link in the notebook catalogue.
2. In Colab, select **Runtime > Run all**, or execute the cells one at a time.
3. If the notebook expects a local file, upload it to the path shown in the **Data or service required** column.
4. Install any packages requested by the notebook when prompted.

Changes made in Colab are not automatically saved back to this repository. Use **File > Save a copy in GitHub** or download the edited notebook when you want to retain them.

## Run locally

Clone the repository and launch Jupyter:

```bash
git clone https://github.com/gitguy007/2026-ColabWorks.git
cd 2026-ColabWorks

python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
python -m pip install --upgrade pip
python -m pip install jupyter pandas numpy matplotlib seaborn scikit-learn
jupyter notebook
```

Dependencies vary by notebook. Install additional libraries referenced in the selected notebook, such as TensorFlow/Keras, NLTK, spaCy, TextBlob, Textacy, Gensim, WordCloud, pyLDAvis, Groq, or the external knowledge-extraction package.

> [!NOTE]
> The notebooks were created at different times and do not currently share a pinned environment. Older examplesâ€”particularly the Reuters NLP and customer-segmentation notebooksâ€”may use APIs that have changed in recent library releases. Google Colab is the recommended starting environment, but minor compatibility updates may still be required.

## Files and credentials

Some notebooks need inputs that are not stored in this repository:

- Upload `Airbnb_Open_Data.csv` and `Zomato-data-.csv` into Colab's `sample_data` directory for their respective EDA notebooks.
- Upload an invoice image named `Invoice.jpg` for the OCR notebook, or update `image_path` in the notebook.
- Upload a PDF as `input/PO.pdf` for the knowledge-extraction example, or update the input path.
- Store API credentials in Colab Secrets or environment variables. Never paste real credentials into notebook cells or commit them to Git.

For the Groq OCR notebook, create a Colab secret named `GROQ_API_KEY` and grant the notebook access to it. The knowledge-extraction notebook supports standard OpenAI or Azure OpenAI configuration through the source project's environment settings.

## Repository structure

```text
2026-ColabWorks/
â”œâ”€â”€ BizAnalytics_W01_Bike_Sharing.ipynb
â”œâ”€â”€ BizAnalytics_W02_Reuters_Authorship.ipynb
â”œâ”€â”€ BizAnalysis_W04_Customer_Segmentation.ipynb
â”œâ”€â”€ BizAnalysis_Demand_Forecasting.ipynb
â”œâ”€â”€ MLSeries_AirBnB_Booking_Analysis_using_EDA.ipynb
â”œâ”€â”€ MLSeries_Zomato_Data_Analysis_Using_Python.ipynb
â”œâ”€â”€ 20260617_ColabWorks!_Groq_OCR.ipynb
â”œâ”€â”€ ColabWorks!_Knowledge_Extraction_Using_Dynamic_Schema_Generation.ipynb
â””â”€â”€ README.md
```

## Responsible use

- Use synthetic, public, or properly authorised data.
- Remove or mask personal, financial, and confidential information before uploading documents to third-party AI services.
- Review AI-extracted results before using them in business processes; OCR and LLM outputs can be incomplete or incorrect.
- Check the terms, licences, and attribution requirements of each external dataset, article, and source repository referenced in the notebooks.

## Contributing

Contributions are welcome. When adding or updating a notebook:

1. Clear credentials, tokens, and sensitive output.
2. Add a short introduction describing the objective, dataset, and expected result.
3. Include installation cells for non-standard dependencies.
4. Add an **Open in Colab** badge using the notebook's exact filename.
5. Run the notebook from top to bottom before submitting a pull request.

## Acknowledgements

Several notebooks adapt learning material, datasets, or examples from external authors and repositories. The source links and credits retained inside each notebook remain the authoritative attribution for that work.

## Licence

No licence file is currently included. Unless a licence is added, normal copyright restrictions apply. External datasets and adapted examples remain subject to their respective licences and terms.

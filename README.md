# Analysis of Migration Discourse in the Media using Computational Linguistics

This repository contain the code used to create a final report (`geographic_analysis_immigration_discourse.pdf`) for Matthew Denny's PPOL628 - Text as Data: Computational Linguistics for Social Sciences course in Spring 2021. I was interested in whether or not the source or destination region of immigration would affect the discourse surrounding the immigrants, particularly in the news media.

I use a corpus of nearly 11,000 news articles and accompanying metadata (author, date, etc.) downloaded from ProQuest. These articles were associated with English-language keywords "migrant", "immigrant", "immigration", "migration", and "border." Since the articles were downloaded as text files containing 500 articles each, I needed to split the text files into individual articles (`split_data.py`) and extract the article text and metadata (`Read_Initial_Corpus.R`) into a single dataframe. I then created cleaned the text further and created regional variables based on the presence of location keywords in the metadata, and visualized the results in an exploratory analysis (`clean_preprocess_viz.R.R`).

Finally, I ran 11 logistic regression models to attempt to predict these regional variables (see the `supervised_models` directory), and use cosine similarity to compute the top-weighted terms from each regional model. These top-weighted terms tended to be similar for regions that are more closely linked geopolitically, and different for regions with a large immigration corridor, such as the US and Mexico.


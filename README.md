# Google Play Store Apps: Exploratory Data Analysis

An exploratory analysis of 2.3 million Google Play Store apps to understand which categories are crowded, which ones capture the most installs, and how complete the store's data is.

**Tools:** Python (pandas, NumPy, Matplotlib, Seaborn, Plotly) in a Jupyter notebook

## Business question

If you were planning a new app, where is the competition heaviest, and where is user demand concentrated?

## Approach

1. Loaded the dataset (2,312,944 apps, 24 columns) and profiled column types and missing values.
2. Counted apps by category, content rating and developer.
3. Summed maximum installs by content rating, category and last-update date to see where demand sits.
4. Visualized the content-rating mix (histogram) and compared rating counts across three categories: Tools, Social and Beauty (pie chart).

## Key findings

- **Education is the most crowded category** with 241,090 apps (10% of the store), followed by Music & Audio (154,906) and Tools (143,988).
- **Number of apps is not the same as demand.** The two biggest category groups by installs are Tools and Communication apps rated "Everyone", with about 116 billion and 68 billion maximum installs. Education, despite having the most apps, doesn't make the top five.
- **Almost everything is rated "Everyone."** That covers 87% of apps (2,022,089). Teen is a distant second at 196,375.
- **A few companies publish thousands of apps.** The top developers by app count are platforms that publish apps on behalf of their clients. Classplus alone accounts for 10,345 apps and Subsplash for 7,570.
- **Data gaps are large.** A third of apps (760,835) list no developer website, and 18% (420,953) have no privacy policy. Rating data is missing for 22,883 apps.

## Takeaways

1. **Crowded is not the same as attractive.** A new Education app enters the most saturated category, while Tools and Communication show far more install demand per category.
2. **The missing privacy policies are a compliance signal.** Nearly one in five apps has no privacy policy listed, which matters for anyone assessing app quality or risk.
3. **Count publishers carefully.** Because platform publishers inflate developer counts, any "top developer" ranking should group or exclude them.

## Next steps

- Normalize installs per app within each category to compare demand fairly.
- Compare free vs paid apps and the effect of in-app purchases on ratings.
- Model what predicts a high rating (category, size, update frequency, ads).

## How to run

The dataset is not included in this repo because of its size (2.3M rows). Download the Google Play Store apps dataset from Kaggle, save it as `google_play.csv` next to the notebook, and run `Google_Play_Store.ipynb`.

## Files

| File | Contents |
|---|---|
| `Google_Play_Store.ipynb` | Full analysis with code, outputs and charts |

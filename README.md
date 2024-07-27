# Marathon Data Analysis

This repository contains a Jupyter Notebook for analyzing marathon data, including various statistics and visualizations.

## Contents

- `MarathonAnalysis.ipynb`: Jupyter Notebook containing the code and analysis for the marathon data.
- `data/`: Directory containing the input data files (if applicable).

## Data Description

The dataset includes various details about marathon events and athlete performances. The key columns in the dataset are:

- `Year of event`: Year in which the marathon event took place.
- `Event dates`: Specific dates of the marathon events.
- `Event name`: Names of the marathon events.
- `Event distance/length`: Distance or length of the marathon events.
- `Event number of finishers`: Number of athletes who finished the marathon.
- `Athlete performance`: Performance time of the athletes.
- `Athlete gender`: Gender of the athletes.
- `Athlete average speed`: Average speed of the athletes.
- `Athlete ID`: Unique identifier for each athlete.

## Analysis Summary

The analysis in the notebook covers the following:

1. **Data Cleaning and Preparation**:
    - Handling missing values.
    - Renaming columns for consistency and readability.

2. **Data Visualization**:
    - Distribution of athlete average speed for specific race lengths.
    - Various plots to visualize the data trends and patterns.

3. **Statistical Analysis**:
    - Calculation of summary statistics for different groups of data.
    - Analysis of athlete performance based on different event lengths.

## Key Functions and Code Snippets

- **Renaming Columns**:
    ```python
    df2 = df2.rename(columns={
        'Year of event': 'year',
        'Event dates': 'race_day',
        'Event name': 'race_name',
        'Event distance/length': 'race_length',
        'Event number of finishers': 'race_number_of_finishers',
        'Athlete performance': 'athlete_performance',
        'Athlete gender': 'athlete_gender',
        'Athlete average speed': 'athlete_average_speed',
        'Athlete ID': 'athlete_id'
    })
    ```

- **Filtering Data and Plotting**:
    ```python
    import seaborn as sns
    import matplotlib.pyplot as plt

    filtered_df = df3[df3['race_length'] == '50mi']
    sns.displot(filtered_df['athlete_average_speed'])
    plt.show()
    ```





## Acknowledgements

- This project uses data from marathon events. The data is hypothetical and created for demonstration purposes.


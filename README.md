## README: Class 1 Survey Analysis (C1survey)

### Overview
This project is an analysis of a survey dataset (`Class 1 Survey Fall 2024_di.csv`) that was collected from the Fall ADA 2024 class. The code provides an  analysis of various aspects of the data, including renaming columns, cleaning data, and exploring interesting relationships such as the preference for pets based on whether individuals are "larks," "owls," or "hummingbirds."

### Dataset
The dataset used in this analysis contains responses from 29 individuals with 30 variables related to their preferences, habits, experience, hopes and background.

### Code

1. **Loading dataset**: The dataset is loaded from a GitHub repository using the `read_csv` function, creating a dataframe called `C1survey`.

2. **Dimensions**:
   - Number of observations and variables in the dataset are determined using the `dim()` function.

3. **Renaming Columns**:
   - Column names are shortened (e.g., renaming "Do you like cats?" to `like_cats`).

4. **Determining variable Types**:
   - Code to determine the types of variables (factor, integer, numeric, character) using `summary()` and `sapply()`.

5. **Handling Birth Day and Month**:
   - Checked for unusual or missing values in the `birth_day` and `birth_month` columns.
   - Converted these columns to numeric for analysis.
   - Calculated the median values for birth day and month.

6. **Seasonal Analysis**:
   - Created a new variable `bseason` to classify respondents into the four seasons (Winter, Spring, Summer, Fall) based on their birth month.
   - A table was generated to display the distribution of respondents across seasons, and the total count for each season was calculated using `addmargins()`.

7. **Pet Preference Analysis**:
   - Created a new variable `pet_pref` to indicate whether respondents prefer "Both" cats and dogs, "Cats," "Dogs," or "Neither."
   - Analyzed the relationship between sleep types (larks, owls, hummingbirds) and pet preferences.
   - Summarized the data into a table, showing the distribution of pet preferences by sleep type.

### Findings
- **Pet Preferences**:
   - Hummingbirds have the highest number of respondents generally and who prefer neither cats nor dogs (6).
   - Larks show the least interest in pets, with only 2 respondents liking both cats and dogs and no one preferring only one pet.
   - Owls exhibit more diverse pet preferences, with a moderate number liking both pets (3), only dogs (3), and neither (5).
   - Most respondents prefer neither cats nor dogs, followed by those who like both pets.
   

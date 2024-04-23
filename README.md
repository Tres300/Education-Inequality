# Education-Inequality
## Description
Data Science exploration project to answer the question: Is school performance predicted by socioeconomic factors?

## Data Preparation
The notebook `Education_Inequality_Data_Preparation.ipynb` was used to determine that both data sets are of appropriate quality. The clean data set was split 80/20 into training and testing datasets. The following changes/preperations were made:
*   Rename the edgap columns `NCESSCH School ID`, `CT Pct Adults with College Degree`,`CT Unemployment Rate`, `CT Pct Childre In Married Couple Family`, `CT Median Household Income`, `School ACT average (or equivalent if SAT score)`, `School Pct Free and Reduced Lunch` to `id`, `percent_college`, `rate_unemployment`, `percent_married`, `median_income`, `average_act`, `percent_lunch`
*   Rename the school_info columns `SCHOOL_YEAR`, `NCESSCH`, `MSTATE`, `MZIP`, `SCH_TYPE_TEXT`, `LEVEL` to `year`, `id`, `state`, `zip_code`, `school_type`, `school_level`
*   All columns not renammed in a dataset were dropped.
*   Negative average_act and percent_lunch values were dropped.
*   Both datasets were joined on `id` using an inner-join.
*   The resulting data was split 80/20 into training and testing datasets.
*   The numeric values training and testing data were normalized using the mean and std of the training data, except average_act.

## Clean Data
`clean_edu_ineq_normalized_train.csv `is the clean data file for training created by `Education_Inequality_Data_Preparation.ipynb`.

`clean_edu_ineq_normalized_test.csv` is the clean data file for testing created by `Education_Inequality_Data_Preparation.ipynb`.

`clean_edu_ineq_train_mean.csv` is the mean vector of the training data.

`clean_edu_ineq_train_std.csv` is the std vector of the training data.

## Data Sources
### EdGap data
`EdGap_data.xlsx` is the data set containing information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district in the year 2016.

All socioeconomic data (household income, unemployment, adult educational attainment, and family structure) are from the Census Bureau’s American Community Survey.

[EdGap.org ](https://www.edgap.org/#5/37.875/-96.987) report that ACT and SAT score data is from each state’s department of education or some other public data release. The nature of the other public data release is not known.

[EdGap.org](https://www.edgap.org/#5/37.875/-96.987) do not indicate that they processed the data in any way. The data were assembled by the [EdGap.org](https://www.edgap.org/#5/37.875/-96.987) team. Given the public nature of the data, the original data sources can be consulted to check the quality of the data.

Downloaded from: [https://github.com/galenegan/DATA-3320/blob/main/weather/seattle_rain.csv](https://github.com/galenegan/DATA-3320/raw/main/education/EdGap_data.xlsx)

### School information data
`ccd_sch_029_1617_w_1a_11212017.csv` is the data set that contains basic information about each school from the [National Center for Education Statistics](https://nces.ed.gov/ccd/pubschuniv.asp).

This data set consists of basic identifying information about schools and can be assumed to be of reasonably high quality.

The data set ccd_sch_029_1617_w_1a_11212017.csv is too large for GitHub and can be accessed from the drive link:

Drive link: [https://drive.google.com/file/d/1HvW2w-o2XZzCm4KTvnb1Bb3BvoAa14BP/view?usp=sharing](https://drive.google.com/file/d/1HvW2w-o2XZzCm4KTvnb1Bb3BvoAa14BP/view?usp=sharing)

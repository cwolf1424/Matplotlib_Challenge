# Matplotlib_challenge
Challenge assignment for Matplotlib

In this challenge...

--------------------------------------------------
Setup
--------------------------------------------------

In the section finding the duplicate mouse, I borrowed from this website: 

https://www.statology.org/pandas-find-duplicates/

the way finding duplicate entires work to create:

duplicate_etries = merged_results_df[merged_results_df.duplicated(['Mouse ID', 'Timepoint'])]

--------------------------------------------------
Bar and Pie Charts
--------------------------------------------------

In the section creating the first bar chart (using pandas), I borrowed from this website:

https://stackoverflow.com/questions/21487329/add-x-and-y-labels-to-a-pandas-plot

the way of setting axis labels to create:

chart_df_bar1.set_ylabel("Rows of Data")



In the section creating the first bar chart (using pandas), I borrowed from this website:

https://stackoverflow.com/questions/14824456/edit-the-width-of-bars-using-pd-dataframe-plot

the way of changing width to create:

chart_df_bar1 = chart_df.plot (kind="bar", title="Rows of Data Per Regimen", legend=False, width=.75)

--------------------------------------------------

--------------------------------------------------
In the section , I borrowed from this website:

https://stackoverflow.com/questions/14824456/edit-the-width-of-bars-using-pd-dataframe-plot

the way of  to create:


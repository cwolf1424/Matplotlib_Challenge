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



In the section creating the first pie chart (using pandas), I borrowed from this website:

    https://www.plus2net.com/python/pandas-dataframe-plot-pie.php

the way of adding percents to create:

    autopct='%1.1f%%'


--------------------------------------------------
Quartiles, Outliers and Boxplot
--------------------------------------------------
In the section preparting for the for loop, I borrowed from learning assistant Sathwik:

    result = pd.merge (left, right, how="left" on =["key1", "key2"])

the way of merging multiple columns to create:

    new_cln_merged_results_df = pd.merge(cln_merged_results_df,grouped_final_tumor_volume_df, on = ["Mouse ID","Timepoint"], how = "right")

and he also helped me realize I needed to merge right on:

    new_cln_merged_results_df = pd.merge(cln_merged_results_df,grouped_final_tumor_volume_df, on = ["Mouse ID","Timepoint"], how = "right")


In the section within the for loop, I borrowed from the week 5 class activity "03-Stu_Summary_Stats_Python" solved file:

    # Determine if there are any potential outliers in the average occupancy in California
    quartiles = california_data['AveOccup'].quantile([.25,.5,.75])
    lowerq = quartiles[0.25]
    upperq = quartiles[0.75]
    iqr = upperq-lowerq

    print(f"The lower quartile of occupancy is: {lowerq}")
    print(f"The upper quartile of occupancy is: {upperq}")
    print(f"The interquartile range of occupancy is: {iqr}")
    print(f"The the median of occupancy is: {quartiles[0.5]} ")

    lower_bound = lowerq - (1.5*iqr)
    upper_bound = upperq + (1.5*iqr)
    print(f"Values below {lower_bound} could be outliers.")
    print(f"Values above {upper_bound} could be outliers.")

    outlier_occupancy = california_data.loc[(california_data['AveOccup'] < lower_bound) | (california_data['AveOccup'] > upper_bound)]
    outlier_occupancy

to create:

    quartiles = treatment_vol_data.quantile([.25,.5,.75])
    lowerq = quartiles[0.25]
    upperq = quartiles[0.75]
    iqr = upperq-lowerq

    print(f"The lower quartile of {treatment} final tumor volume is: {lowerq}")
    print(f"The upper quartile of {treatment} final tumor volume is: {upperq}")
    print(f"The interquartile range of {treatment} final tumor volume is: {iqr}")
    print(f"The the median of {treatment} final tumor volume is: {quartiles[0.5]} ")

    lower_bound = lowerq - (1.5*iqr)
    upper_bound = upperq + (1.5*iqr)
    print(f"Values below {lower_bound} for {treatment} could be outliers.")
    print(f"Values above {upper_bound} for {treatment} could be outliers.")

    outlier_tumor_volumes = treatment_vol_data.loc[(treatment_vol_data < lower_bound) | (treatment_vol_data > upper_bound)]
    print(f"Potential outliers for {treatment} (if any): {outlier_tumor_volumes}")
    print("")
    print("---------------------------------------------------------")
    print("")


In the section editing the box plots, I borrowed from this website:

    https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.xticks.html

the way of changing x-ticks to create:

    plt.xticks ([1,2,3,4], promising_treatments)


In the section editing the box plots, I borrowed from this website:

    https://matplotlib.org/stable/gallery/statistics/boxplot_demo.html

the way of changing x-ticks to create:

    plt.boxplot (tumor_vol_data, 0, 'r*')


TEST
    
# Nashville Housing Dataset Cleaning and Analysis

This repository documents the data cleaning process and subsequent analysis performed on the Nashville Housing dataset using SQL. The goal was to preprocess and organise the dataset for more effective analysis. Below are the steps taken along with some insights gained from the data.

## Data Cleaning Steps

1. Changing Date Format
I started by adding a new column, SaleDateConverted, to store the sale date in a standardized format. This was achieved using the CONVERT function.

2. Populating Property Address
To ensure complete property addresses, I identified missing values using a self-join and populated them with data from corresponding rows.

3. Splitting Property Address
The property address was split into individual columns: PropertySplitAddress and PropertySplitCity, providing a structured representation of address components.

4. Splitting Owner Address
Similar to property addresses, the owner address was split into OwnerSplitAddress, OwnerSplitCity, and OwnerSplitState columns using the PARSENAME function.

5. Standardizing "Sold as Vacant"
The values in the "Sold as Vacant" column were standardized to "Yes" and "No" by replacing "Y" and "N," ensuring consistency.

6. Removing Duplicates
Duplicates were identified using a common table expression (RowNumCTE), and redundant rows were removed while preserving the most relevant information.

7. Dropping Unused Columns
Columns that were no longer needed, such as OwnerAddress, TaxDistrict, PropertyAddress, and SaleDate, were dropped from the dataset.

## Analysis Insights

The dataset was standardized for easier analysis with consistent date and address formats.

Property and owner addresses were split into individual components, enhancing data organization and querying.

"Sold as Vacant" values were made consistent, facilitating accurate analysis.

Duplicates were removed, ensuring each record was unique and eliminating redundancy.

Unused columns were dropped, reducing dataset clutter and focusing on relevant attributes.

## Contact

Feel free to explore the SQL queries provided in this repository for a comprehensive understanding of the data cleaning process and analysis steps performed on the Nashville Housing dataset.

For more details, you can refer to my SQL notebook in this repository - https://github.com/AmritBinning/NashVille_Housing_Data_Cleaning_Queries.

Feel free to reach out if you have any questions or insights regarding this analysis at amritbinning14@gmail.com!

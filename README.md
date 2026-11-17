# Global Airbnb Performance Dashboard (Power BI)

An interactive 3-page Power BI dashboard analysing Airbnb listings, reviews and hosts across 10 major cities, covering listing growth, market share, ratings, seasonality and host trust.

![Dashboard page 1](images/airbnb_page1.png)

## Objective

Understand how Airbnb grew, which cities dominate the market, how guests rate their stays, and how reviewing behaviour and host trust differ across cities.

## Dataset

| File | Rows | Description |
|---|---|---|
| `Listings.csv` | 279,712 | Listing details: city, room and property type, price, host info, review scores |
| `Reviews.csv` | 5,373,143 | One row per review: listing, reviewer and date (Nov 2008 to Mar 2021) |

- **Cities (10):** Paris, New York, Sydney, Rome, Rio de Janeiro, Istanbul, Mexico City, Bangkok, Cape Town, Hong Kong
- **Hosts:** 182,024 | **Property types:** 144
- Data dictionaries are in `data/`.

> **Note:** The raw CSVs are too large for GitHub (152 MB and 244 MB). Download them from: `ADD-DATASET-LINK-HERE` and place them in the `data/` folder.

## Dashboard Pages

1. **Growth:** new listings per year by room type, with the stages of Airbnb's growth up to COVID-19
2. **Market and Ratings:** market share by city (Superhost vs non-Superhost) and a heat map of ratings for accuracy, cleanliness, communication, location and value
3. **Behaviour and Trust:** review frequency per reviewer, review seasonality by city, and host identity and profile verification

## Key Insights

- **Market concentration:** Paris, New York and Sydney together hold 48.4% of all listings and about 59% of all reviews. Paris has the most listings and reviews.
- **Growth cycle:** new listings peaked in 2015, dipped in 2016 to 2017 and recovered slightly before the COVID-19 drop in 2020.
- **Ratings:** Mexico City and Rio de Janeiro are the best rated; Hong Kong and Istanbul are the lowest. Cleanliness and value for money score lowest across most cities.
- **Superhosts:** about 18% of listings are run by Superhosts, who average a 97.0 rating compared with 92.3 for other hosts (scale of 100).
- **Reviewer behaviour:** 86.5% of reviewers wrote only one review, and 98.8% wrote three or fewer.
- **Seasonality:** Paris and Rome dominate review share from April to August (European summer), while New York rises in November and December.
- **Trust:** about two-thirds of hosts are identity-verified and have a profile picture.

## Data Limitations

- `price` is stored in each city's **local currency**, so prices cannot be compared across cities without converting to one currency. Price comparisons should be made within a city.
- Many listings have no review scores (about 91,000 missing), so ratings reflect only listings that have been reviewed.

## Tools Used

Power BI Desktop, Power Query, DAX

<!-- TODO: if you also clean or query the data with Python (Pandas) or SQL, add them to Tools Used and describe it in a short "Analysis Steps" section -->

## Repository Structure

```
├── data/
│   ├── Listings_data_dictionary.csv
│   └── Reviews_data_dictionary.csv
├── dashboard/
│   └── Airbnb_Dashboard.pbix
├── images/
│   ├── airbnb_page1.png
│   ├── airbnb_page2.png
│   └── airbnb_page3.png
└── README.md
```

## Author

**Rishabh Jain** | B.Tech CSE (Data Science), Chandigarh Group of Colleges, Landran
[LinkedIn](https://www.linkedin.com/in/YOUR-LINKEDIN) | rishabh151jain@gmail.com

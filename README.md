# AirBnb_Seattle_Data_Analysis
Udacity Introduction to Data Science Blog Post Project

This repository is used for analyzing AirBnb data.

## WHAT'S INCLUDED
AirBnb_Seattle_Data_Analysis/
|-- AirBnB_Seattle_Data_Analysis.ipynb
|-- Data/
|   |-- listings.csv

## DOCUMENTATION
In order to run the script, download the files (keep the folder hierarchy as is) under Jupyter directory, open the script file in the Notebook and run.

This project follows CRISP-DM methodology, and the following explains each phase:
### BUSINESS UNDERSTANDING
  Use the available datasets to find popular listings and find the differences from non-popular listings.  And comparing the metadata in each group will help identifying what factors may help booking the property.  In this analysis, the property with 80% or more booking is defined as popular listing and less than 80% booking is grouped in non-popular listing.
  
### DATA UNDERSTANDING
  Datasets used in this analysis was collected from this source:  http://insideairbnb.com/get-the-data.html
  File location:  
      http://data.insideairbnb.com/united-states/wa/seattle/2021-02-21/data/listings.csv.gz
      http://data.insideairbnb.com/united-states/wa/seattle/2021-02-21/data/calendar.csv.gz
  
  The data files were compressed CSV format.

""""listings.csv""""
  The file contains 4197 records and 74 fields.  The field list is as follows:
'id',  'listing_url',  'scrape_id',  'last_scraped',  'name',  'description',  'neighborhood_overview',  'picture_url',  'host_id',  'host_url',  'host_name',  'host_since',  'host_location',  'host_about',  'host_response_time',  'host_response_rate',  'host_acceptance_rate',  'host_is_superhost',  'host_thumbnail_url',  'host_picture_url',  'host_neighbourhood',  'host_listings_count',  'host_total_listings_count',  'host_verifications',  'host_has_profile_pic',  'host_identity_verified',  'neighbourhood',  'neighbourhood_cleansed',  'neighbourhood_group_cleansed',  'latitude',  'longitude',  'property_type',  'room_type',  'accommodates',  'bathrooms',  'bathrooms_text',  'bedrooms',  'beds',  'amenities',  'price',  'minimum_nights',  'maximum_nights',  'minimum_minimum_nights',  'maximum_minimum_nights',  'minimum_maximum_nights',  'maximum_maximum_nights',  'minimum_nights_avg_ntm',  'maximum_nights_avg_ntm',  'calendar_updated',  'has_availability',  'availability_30',  'availability_60',  'availability_90',  'availability_365',  'calendar_last_scraped',  'number_of_reviews',  'number_of_reviews_ltm',  'number_of_reviews_l30d',  'first_review',  'last_review',  'review_scores_rating',  'review_scores_accuracy',  'review_scores_cleanliness',  'review_scores_checkin',  'review_scores_communication',  'review_scores_location',  'review_scores_value',  'license',  'instant_bookable',  'calculated_host_listings_count',  'calculated_host_listings_count_entire_homes',  'calculated_host_listings_count_private_rooms',  'calculated_host_listings_count_shared_rooms',  'reviews_per_month'

  The following columns did not contain any values and were removed:
        'bathrooms', 'calendar_updated'
        
 """"calendar.csv""""
  The file contains 1531652 rows and 7 columns.  The field list is as follows:
'listing_id', 'date', 'available', 'price', 'adjusted_price', 'minimum_nights', 'maximum_nights'  
  
 ### DATA PREPARATION
  listings.csv and calendar.csv were used in this analysis as it contains information about each property and the number of days they are booked.  calendar.csv was used to determine the timeframe of the booking in this dataset.

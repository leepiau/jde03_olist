# jde03_olist
Inisght Igniters JDE03

**geolocation table:**
24-04-26:
1. One zip_prefix can cover multiple locations (combinations of lat/lng)
2. The same combination of lat/lng can have multiple zip_prefixes
3. The same combination of lat/lng can only be in one city
4. One city can cover multiple lat/lng combinations
   > Therefore we need a composite key of zip_prefix, lat, lng, city
5. Replaced geolocation_city with customer_city where customer_city exists for matching zip_prefix_code > merged_df
6. Replaced geolocation_city in merged_df with seller_city for matching zip_prefix_code where customer_city did not exist
7. Removed duplicates based on zip_prefix, lat, lng
8. Removed complete duplicates

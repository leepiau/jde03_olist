# jde03_olist
Inisght Igniters JDE03

**geolocation table:**
24-04-26:
1. One zip_prefix can cover multiple locations (combinations of lat/lng) - zip_prefix CANNOT be Primary Key
2. The same combination of lat/lng can have multiple zip_prefixes - lat/lng CANNOT be composit Key
3. One city can cover multiple lat/lng combinations - lat/lng/city CANNOT be composite key
4. THerefore a valid composite key is (zip_prefix, lat, lng)
5. Replaced geolocation_city with customer_city where customer_city exists for matching zip_prefix_code > merged_df
6. Replaced geolocation_city in merged_df with seller_city for matching zip_prefix_code where customer_city did not exist
7. Removed duplicates based on zip_prefix, lat, lng
8. Removed complete duplicates
9. Sorted by zip_prefix and reindexed

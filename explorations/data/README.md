# ct_load_weather_hourly_2023_2026.csv

One row per hour (UTC, start of the hour), January 2023 to October 16, 2026.

| column | meaning | source |
|---|---|---|
| `hour_utc` | start of the hour, UTC | - |
| `load_mw` | Connecticut zone load (MW). 2023-2025: ISO-NE real-time hourly demand (the Lab 5 file). 2026: ISO-NE five-minute *estimated* Connecticut native load, averaged to the hour and divided by 1.0113 so it lines up with the earlier series (the two agree to r = 0.9994 on 6,579 overlapping hours). | ISO New England |
| `temp_f` | air temperature at Bradley Airport, °F | Iowa State Mesonet (NWS/FAA reports), cleaned as in Lab 5 |
| `cloud_cover_pct` | sky covered by the thickest reported cloud layer, % | same |

Used by `../tomorrow_best_forecast.ipynb`, which tops it up with the last 10 days at run time.

# Data

## Dataset: Steam-200k User Game Dataset

**Source:** [Kaggle — Steam Video Games](https://www.kaggle.com/datasets/tamber/steam-video-games)  
**Format:** CSV (`steam-200k.csv`)  
**Size:** ~4MB | 200,000 rows  
**License:** Open (Kaggle)

### Schema
The dataset has no header — columns are positionally defined:

| Position | Name | Type | Description |
|----------|------|------|-------------|
| 0 | user_id | int | Unique user identifier |
| 1 | game_title | string | Name of the game |
| 2 | behavior | string | Interaction type: `purchase` or `play` |
| 3 | hours | float | Hours played (0.0 for purchase-only records) |
| 4 | _ | int | Unused column (always 0) |

### Setup
```bash
kaggle datasets download tamber/steam-video-games
unzip steam-video-games.zip -d data/
mv data/steam-200k.csv data/steam-200k.csv
```

Upload to Databricks DBFS or configure the path in the notebook before running.

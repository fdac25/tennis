# Data Folder

This project uses datasets based on **Roland Garros** tennis data.

## 1️⃣ Raw Shot-Level Dataset

The raw **Roland Garros** shot dataset (`tennis-m-shots-rg.csv.gz`) is available at:
[OneDrive link](https://drive.google.com/file/d/14sr92fnOyu3p9tAH0nU7AnVDe_ueB145/view?usp=drive_link)

Place it in `data/raw/` before use.

Then load it in Python using:

```python
import pandas as pd
df = pd.read_csv("data/raw/tennis-m-shots-rg.csv.gz", compression="gzip")
```

## 2️⃣ Processed Point-Level Dataset

The processed dataset (`point_level_rg.csv.gz`) - created from the raw shot data - is also available at:
[OneDrive link](https://drive.google.com/file/d/14sr92fnOyu3p9tAH0nU7AnVDe_ueB145/view?usp=drive_link)

Place it in `data/processed/` before use.

Then, as before, load with:

```python
import pandas as pd
df = pd.read_csv("data/processed/point_level_rg.csv.gz", compression="gzip")
```

**Note**: pathname (`data/...`) may need to be preceded by some number of `../` depending on the file where it's used.

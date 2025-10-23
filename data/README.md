# Data Folder

The raw **Roland Garros** shot dataset (`tennis-m-shots-rg.csv.gz`) is available at:
[OneDrive link](https://drive.google.com/file/d/14sr92fnOyu3p9tAH0nU7AnVDe_ueB145/view?usp=drive_link)

Place it in `data/raw/` before running notebooks.

Then load it in Python using:

```python
df = pd.read_csv("data/raw/tennis-m-shots-rg.csv.gz", compression="gzip")
```

# dc_reflib
Data causality reference library

This repo is a collection of datasets to help with the development of data causality tools. [Data causality](https://en.wikipedia.org/wiki/Exploratory_causal_analysis) often relies on "reasonable" notions of causality. This collection of datasets have their concepts of causality built-in&mdash;literally in the case of the Parquet files&mdash;which means they are suitable for training and testing data causality computational tools.

## Example usage
The following Python code
```python
import pandas as pd
import pyarrow as pa
df = pd.read_parquet('parquet_sets/bivariate/bivariate_0.parquet')
print(df.describe().to_markdown())
```
yields
|       |    cause |    effect |
|:------|---------:|----------:|
| count |  349     | 349       |
| mean  |  332.47  |   8.04155 |
| std   |  339.298 |   1.51851 |
| min   |    0     |  -4.8     |
| 25%   |   70     |   7.5     |
| 50%   |  255     |   8.3     |
| 75%   |  490     |   8.9     |
| max   | 2960     |  10.8     |

## Data formats
The data is currently in text files and [Parquet](https://arrow.apache.org/docs/index.html). Examples of working with parquet files are available in several different languages including [Python](https://arrow.apache.org/cookbook/py/), [R](https://arrow.apache.org/cookbook/r/), [C++](https://arrow.apache.org/cookbook/cpp/), and [Rust](https://docs.rs/crate/arrow/latest).

## Full documentation
The full documentation, including discussions of the operational definitions of causality used in each data set are available here: 
...TBD...

---
<img src=https://img.shields.io/badge/everything_cool-yeah-purple />

# Collection of useful Python snippets that you can understand in 30 seconds or less.

## Date 

## Datetime

```python
from datetime import datetime, timedelta

DATE_FORMAT = '%Y%m%d'
# show today with yyyymmdd format by string format time func
TODAY = datetime.today().strftime(DATE_FORMAT)

# convert string datetime to date obj by string parse time func
datetime_obj = datetime.strptime('20170111', DATE_FORMAT)
```

## File operation

### Delete file

Delete a file which may not exist.

```python
import os

try:
    os.remove(filename)
except OSError:
    pass
```

## List operation

### Two lists substraction

- Using set to subtract two list.

```python
list(set(origin_all_feature_list) - set(remove_nan_feature_list))
```

## Pandas

### Import data

```python
import pandas as pd

path = 'data.csv'

### Import data without first column as header
data = pd.read_csv(path, header=None)

print data

```
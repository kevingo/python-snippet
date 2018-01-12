# Collection of useful Python snippets that you can understand in 30 seconds or less.

## Date 

## Datetime

```python
from datetime import datetime, timedelta

# show today with yyyymmdd format
TODAY = datetime.today().strftime('%Y%m%d')

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
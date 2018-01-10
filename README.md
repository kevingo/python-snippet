# Collection of useful Python snippets that you can understand in 30 seconds or less.

## File operation

### 

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
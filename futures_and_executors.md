# Futures and Executors

## Topic
Futures abstraction and executor-based concurrency.

---

## Problem Scenario
Run background tasks and retrieve results later.

---

## Code Example

```python
from concurrent.futures import ThreadPoolExecutor

def task():
    return "done"

with ThreadPoolExecutor() as ex:
    future = ex.submit(task)
    print(future.result())


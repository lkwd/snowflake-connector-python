---
name: Bug Report 🐞
about: Something isn't working as expected? Here is the right place to report.
labels: bug, needs triage
---

Please answer these questions before submitting your issue. Thanks!

1. What version of Python are you using (`python --version`)?

2. What operating system and processor architecture are you using (`python -c 'import platform; print(platform.platform())'`)?

3. What are the component versions in the environment (`pip freeze`)?

```
Insert pip freeze's output here.
```

4. What did you do?
If possible, provide a recipe for reproducing the error.
A complete runnable program is good.

5. What did you expect to see?

6. What did you see instead?

7. Can you set logging to DEBUG and collect the logs?

```
import logging
import os

for logger_name in ['snowflake.sqlalchemy', 'snowflake.connector', 'botocore']:
    logger = logging.getLogger(logger_name)
    logger.setLevel(logging.DEBUG)
    ch = logging.StreamHandler()
    ch.setLevel(logging.DEBUG)
    ch.setFormatter(logging.Formatter('%(asctime)s - %(threadName)s %(filename)s:%(lineno)d - %(funcName)s() - %(levelname)s - %(message)s'))
    logger.addHandler(ch)
```

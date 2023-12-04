# ActionsDemo

1. Create **new GitHub**: GitHubActions
2. Create **hw.py** in toplevel including print("Hello SRH!")
3. Create a directory **.github/workflows/** (Slash at end)
4. Create a file **python-script.yml** that includes the action:

```
name: Run Python Script

on:
  workflow_dispatch:
  push:

jobs:
  run-script:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: '3.x'

    - name: Run script
      run: python hello_world.py
```

5. Go to actions, select the action and select **run**

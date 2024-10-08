
# Template Python Operator

Cell-wise mean calculated implemented in Python.

## Python operator - Development workflow

* Set up [the Tercen Studio development environment](https://github.com/tercen/tercen_studio)
* Create a new git repository based on the [template Python operator](https://github.com/tercen/template-python-operator)
* Open VS Code Server by going to: http://127.0.0.1:8443
* Clone this repository into VS Code (using the 'Clone from GitHub' command from the Command Palette for example)
* Load the environment and install core requirements by running the following commands in the terminal:

```bash
pip3 install -r requirements.txt
```

* Develop your operator. Note that you can interact with an existing data step by specifying arguments to the `TercenContext` function:

```python
tercenCtx = ctx.TercenContext()
```

```python
tercenCtx = ctx.TercenContext(
    workflowId="YOUR_WORKFLOW_ID",
    stepId="YOUR_STEP_ID",
    serviceUri = "http://tercen:5400/" # if using the local Tercen instance 
)
```

* Update the requirements.txt file with relevant dependencies
* Push your changes to GitHub: triggers CI GH workflow
* Tag the repository: triggers Release GH workflow
* Go to tercen and install your operator

Check out the [Developer's Guide](https://tercen.github.io/developers_guide/) for more information on how to develop operators.

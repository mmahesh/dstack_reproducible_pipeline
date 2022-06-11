# Reproducible training pipelines with dstack and WandB

The `prepare.py` downloads the required data.

The `train.py` contains all the machine learning components.

In order to automate the workflow, I use `dstack`.

To track the experiment configuration, I use `WandB`.

The workflows can be found at `.dstack/workflows.yaml`.

In order to run the `train` workflow, all you need to do is execute the following command in your terminal:

```bash
dstack run train
```

The `train` workflow has dependency on `prepare` workflow. So, the `prepare` workflow is automatically executed by `dstack`.

If you assigned a tag to the `prepare` workflow, then with the above command `dstack` will not run `prepare` workflow.

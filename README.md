* Deploy infrastructure with terraform:
```
terraform init
terraform apply
```
* Open Azure Portal, navigate to "All resources" tab and select Azure Databricks Service
* Import `ML End-to-End Example.dbc` file as Notebook
* Change next lines in Notebook:
    * cmd 34: `rstate=np.random.RandomState(123)` -> `rstate=np.random.default_rng(123)`
    * cmd 46: `table_path = "dbfs:/<your-value-here>/delta/wine_data"`
* Execute all the steps from "ML End-to-End Example" notebook
* Check results and destroy infrastructure with:
```
terraform destroy
```

In `notebooks/export` you can find exports(`.dbc`, `.html`, `.ipynb`, `.py`) from executed notebook.
In `notebooks/screenshots` you can find run-related images.

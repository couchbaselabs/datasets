# Online Streaming Dataset

_online_streaming.csv_ is a synthetic dataset created by Couchbase. It simulates customer records of a hypothetical online streaming service company. It contains 500,000 customer records.

Download this dataset and load it to your Couchbase cluster using these steps:

1.  Create an _online_streaming_ bucket on your Couchbase cluster.
2.  Import the dataset using this _cbimport_ command:

```bash
cbimport csv -c <cluster> -u <user_name> -p <password> -b online_streaming -d file:///<path_to_downloaded_dataset>/online_streaming.csv --generate-key key_%CustomerID% --infer-types
```

# Insurance Dataset

_insurance.csv_ is a small dataset that is created from public domains to match the dataset provided in the book [Machine Learning With R](https://www.packtpub.com/product/machine-learning-with-r-third-edition/9781788295864) by Brett Lantz. The dataset has been imported from the [open source project](https://github.com/stedy/Machine-Learning-with-R-datasets). The dataset provides the insurance charges for people based on different parameters like age, gender, children, region, etc. It contains 1339 records.

Download this dataset and load it to your Couchbase cluster using these steps:

1.  Create an _insurance_ bucket on your Couchbase cluster.
2.  Import the dataset using this _cbimport_ command:

```bash
cbimport csv -c <cluster> -u <user_name> -p <password> -b insurance -d file:///<path_to_downloaded_dataset>/insurance.csv --generate-key key_#UUID# --infer-types
```

## Notes

Notice the _infer-types_ parameter in the above command. If infer types is set then _cbimport_ will look at each value and decide whether it is a string, integer, or boolean value and put the inferred type into the document.
More information on _cbimport_ is available [here](https://docs.couchbase.com/server/current/tools/cbimport-csv.html).

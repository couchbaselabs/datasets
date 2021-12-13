# Online Streaming Dataset

*online_streaming.csv* is a synthetic dataset created by Couchbase. It simulates customer records of a hypothetical online streaming service company. It contains 500,000 customer records.

Download this dataset and load it to your Couchbase cluster using these steps:
 1. Create an *online_streaming* bucket on your Couchbase cluster.
 2. Import the dataset using this *cbimport* command:
```bash
cbimport csv -c <cluster> -u <user_name> -p <password> -b online_streaming -d file:///<path_to_downloaded_dataset>/online_streaming.csv --generate-key key_%CustomerID% --infer-types
```
Notice the *infer-types* parameter in the above command. If infer types is set then *cbimport* will look at each value and decide whether it is a string, integer, or boolean value and put the inferred type into the document.
More information on *cbimport* is available [here](https://docs.couchbase.com/server/current/tools/cbimport-csv.html).


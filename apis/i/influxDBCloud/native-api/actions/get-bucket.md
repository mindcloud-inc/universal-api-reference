# Get Bucket with InfluxDB Cloud

Retrieves a bucket from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/buckets/:bucketID`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Bucket](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketID` | path | `string` | yes | InfluxDB bucket ID. |

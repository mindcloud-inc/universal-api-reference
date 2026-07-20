# Get Bucket Labels with InfluxDB Cloud

Retrieves bucket labels from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/buckets/:bucketID/labels`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Bucket Labels](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsIDLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketID` | path | `string` | yes | InfluxDB bucket ID. |

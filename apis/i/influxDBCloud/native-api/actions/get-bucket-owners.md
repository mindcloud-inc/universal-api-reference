# Get Bucket Owners with InfluxDB Cloud

Retrieves bucket owners from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/buckets/:bucketID/owners`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Bucket Owners](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsIDOwners)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketID` | path | `string` | yes | InfluxDB bucket ID. |

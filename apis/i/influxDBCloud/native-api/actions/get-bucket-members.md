# Get Bucket Members with InfluxDB Cloud

Retrieves bucket members from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/buckets/:bucketID/members`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Bucket Members](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBucketsIDMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketID` | path | `string` | yes | InfluxDB bucket ID. |

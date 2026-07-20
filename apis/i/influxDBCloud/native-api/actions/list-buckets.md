# List Buckets with InfluxDB Cloud

Retrieves buckets from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/buckets`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Buckets](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetBuckets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of buckets to return. |
| `orgID` | query | `string` | yes | InfluxDB organization ID to list buckets for. |

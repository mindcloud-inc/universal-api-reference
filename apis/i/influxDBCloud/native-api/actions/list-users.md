# List Users with InfluxDB Cloud

Retrieves users from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Users](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetUsers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of users to return. |

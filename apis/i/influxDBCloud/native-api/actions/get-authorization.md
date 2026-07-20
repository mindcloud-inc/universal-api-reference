# Get Authorization with InfluxDB Cloud

Retrieves an authorization from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/authorizations/:authID`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Authorization](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetAuthorizationsID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authID` | path | `string` | yes | InfluxDB authorization ID. |

# Get Organization with InfluxDB Cloud

Retrieves an organization from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgID`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Organization](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | InfluxDB organization ID. |

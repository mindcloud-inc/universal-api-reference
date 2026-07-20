# Get Organization Usage with InfluxDB Cloud

Retrieves organization usage from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgID/usage`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Organization Usage](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgUsageID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | InfluxDB organization ID. |
| `start` | query | `string` | no | RFC3339 start time for the usage window. |
| `stop` | query | `string` | no | RFC3339 stop time for the usage window. |

# List Dashboards with InfluxDB Cloud

Retrieves dashboards from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboards`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Dashboards](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetDashboards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of dashboards to return. |

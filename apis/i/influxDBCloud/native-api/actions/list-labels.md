# List Labels with InfluxDB Cloud

Retrieves labels from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/labels`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Labels](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of labels to return. |
| `orgID` | query | `string` | no | Optional organization ID to scope labels. |

# List Tasks with InfluxDB Cloud

Retrieves tasks from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Tasks](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetTasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of tasks to return. |

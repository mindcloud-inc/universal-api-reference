# List Organizations with InfluxDB Cloud

Retrieves organizations from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Organizations](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | query | `string` | no | Filter organizations by organization ID. |

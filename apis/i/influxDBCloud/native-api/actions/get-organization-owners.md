# Get Organization Owners with InfluxDB Cloud

Retrieves organization owners from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgID/owners`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Organization Owners](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsIDOwners)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | InfluxDB organization ID. |

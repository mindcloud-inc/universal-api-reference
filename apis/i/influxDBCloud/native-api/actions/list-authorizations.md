# List Authorizations with InfluxDB Cloud

Retrieves authorizations from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/authorizations`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [List Authorizations](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetAuthorizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of authorizations to return. |
| `orgID` | query | `string` | no | Organization ID to scope the authorization list. |

# Get Organization Secrets with InfluxDB Cloud

Retrieves organization secrets from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgID/secrets`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Organization Secrets](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgsIDSecrets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | InfluxDB organization ID. |

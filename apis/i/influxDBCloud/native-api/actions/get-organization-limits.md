# Get Organization Limits with InfluxDB Cloud

Retrieves organization limits from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:orgID/limits`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get Organization Limits](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetOrgLimitsID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | InfluxDB organization ID. |

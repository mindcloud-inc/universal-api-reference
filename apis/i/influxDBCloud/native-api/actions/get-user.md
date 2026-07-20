# Get User with InfluxDB Cloud

Retrieves a user from InfluxDB Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userID`
- **Base URL:** `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`
- **Official documentation:** [Get User](https://docs.influxdata.com/influxdb/cloud/api/#operation/GetUsersID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userID` | path | `string` | yes | InfluxDB user ID. |

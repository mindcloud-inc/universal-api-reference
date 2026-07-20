# Generate GUIDs with Tophhie Cloud

Generates one or more GUIDs in Tophhie Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/generate/guid`
- **Base URL:** `https://api.tophhie.cloud`
- **Official documentation:** [Generate GUIDs](https://api.tophhie.cloud/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numberOfGuids` | query | `number` | no | Number of GUIDs to return. Maximum is 500. |

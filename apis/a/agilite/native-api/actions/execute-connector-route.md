# Execute Connector Route with Agilite

Executes a connector route in Agilite by profile and route key.

## Endpoint

- **Method:** `POST`
- **Path:** `/connectors/execute`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Execute Connector Route](https://docs.agilite.io/reference/execute-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile-key` | query | `string` | yes | Unique Connector profile key. |
| `route-key` | query | `string` | yes | Configured connector route key. |
| `data` | body | `object` | no | Optional JSON body values used by the connector profile. |

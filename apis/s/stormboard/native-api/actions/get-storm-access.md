# Get Storm Access with Stormboard

Retrieves your access level for a Storm in Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/storms/:storm_id/access`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Get Storm Access](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |

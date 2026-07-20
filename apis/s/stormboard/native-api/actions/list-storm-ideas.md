# List Storm Ideas with Stormboard

Retrieves ideas from a Storm in Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/storms/:storm_id/ideas`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [List Storm Ideas](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModifiedMin` | query | `string` | no | Return ideas modified since this ISO 8601 timestamp. |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |

# List Storm Participants with Stormboard

Retrieves participants from a Storm in Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/storms/:storm_id/users`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [List Storm Participants](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |

# Get Storm Details with Stormboard

Retrieves Storm details from Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/storms/:storm_id`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Get Storm Details](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |
| `thumbnail` | query | `string` | no | Optional storm thumbnail value. |

# Accept Storm Invite with Stormboard

Accepts a Storm invite in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/storms/:storm_id/invite/accept`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Accept Storm Invite](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |

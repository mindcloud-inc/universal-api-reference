# Decline Storm Invite with Stormboard

Declines a Storm invite in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/storms/:storm_id/invite/decline`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Decline Storm Invite](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |

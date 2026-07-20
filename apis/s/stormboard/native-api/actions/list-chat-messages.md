# List Chat Messages with Stormboard

Retrieves chat messages from a Storm in Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/:storm_id/list`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [List Chat Messages](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storm_id` | path | `number` | yes | Storm ID from the Stormboard share dialog or related storm record. |

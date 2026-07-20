# Initiate Call with CallKeeper

Initiates a new call in CallKeeper.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Initiate Call](https://api.callkeeper.ai/docs#/Calls/initiate_call_calls_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to_number` | body | `string` | yes | Phone number to call. |

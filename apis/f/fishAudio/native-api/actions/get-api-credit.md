# Get API Credit with Fish Audio

Retrieves current API credit balance from Fish Audio.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallet/:user_id/api-credit`
- **Base URL:** `https://api.fish.audio`
- **Official documentation:** [Get API Credit](https://docs.fish.audio/api-reference/endpoint/wallet/get-api-credit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `check_free_credit` | query | `boolean` | no | When true, also returns free-credit availability. |

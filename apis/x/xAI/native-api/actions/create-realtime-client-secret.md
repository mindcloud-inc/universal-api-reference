# Create Realtime Client Secret with xAI

Creates a realtime client secret in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/realtime/client_secrets`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Create Realtime Client Secret](https://docs.x.ai/developers/rest-api-reference/inference/voice#create-realtime-client-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expires_after` | body | `object` | no | Expiration object for the ephemeral client secret. |

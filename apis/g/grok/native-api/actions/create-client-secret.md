# Create Client Secret with Grok

Creates a realtime client secret in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/realtime/client_secrets`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Create Client Secret](https://docs.x.ai/developers/rest-api-reference/inference/voice#create-client-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expires_after.seconds` | body | `number` | no | Seconds until the client secret expires. |

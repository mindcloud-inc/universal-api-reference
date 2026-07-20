# Generate Temporary Token with Deepgram

Creates a temporary token in Deepgram.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/auth/grant`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Generate Temporary Token](https://developers.deepgram.com/reference/auth/tokens/grant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ttl_seconds` | body | `number` | no | Time to live in seconds for the generated token. |

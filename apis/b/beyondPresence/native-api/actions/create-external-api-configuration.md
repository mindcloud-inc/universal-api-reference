# Create External API Configuration with Beyond Presence

Creates a new external API configuration in Beyond Presence.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/external-apis`
- **Base URL:** `https://api.bey.dev`
- **Official documentation:** [Create External API Configuration](https://docs.bey.dev/api-reference/external-apis/create-external-api-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | body | `string` | yes | API key for the external API. |
| `name` | body | `string` | yes | Name of the external API configuration. |
| `type` | body | `string` | no | External API type. |
| `url` | body | `string` | yes | URL of the external API. |

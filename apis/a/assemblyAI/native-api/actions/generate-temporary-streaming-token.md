# Generate Temporary Streaming Token with AssemblyAI

Retrieves a temporary streaming token from AssemblyAI.

## Endpoint

- **Method:** `GET`
- **Path:** `https://streaming.assemblyai.com/v3/token`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Generate Temporary Streaming Token](https://www.assemblyai.com/docs/api-reference/streaming-api/generate-streaming-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expires_in_seconds` | query | `number` | yes | Desired token expiration in seconds. |
| `max_session_duration_seconds` | query | `number` | no | Maximum session duration in seconds for the generated token. |

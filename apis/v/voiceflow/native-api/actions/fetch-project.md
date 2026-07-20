# Fetch Project with Voiceflow

Retrieves exported project files from Voiceflow.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.voiceflow.com/v2/versions/:versionId/export`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Fetch Project](https://docs.voiceflow.com/api-reference/project/fetch-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `versionId` | path | `string` | yes | Voiceflow project version ID, or the alias development or production when used with the projectID header. |
| `prototype` | query | `string` | no | Return the concise .vfr export when true. |

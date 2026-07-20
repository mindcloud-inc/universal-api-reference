# Get Agent Artifact Download URL with Cursor

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/agents/{{id}}/artifacts/download`
- **Base URL:** `https://api.cursor.com`
- **Official documentation:** [Get Agent Artifact Download URL](https://cursor.com/docs/cloud-agent/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the cloud agent that produced the artifact. |
| `path` | query | `string` | yes | Absolute artifact path returned by List Agent Artifacts, for example `/opt/cursor/artifacts/screenshot.png`. |

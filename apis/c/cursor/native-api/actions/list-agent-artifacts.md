# List Agent Artifacts with Cursor

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/agents/{{id}}/artifacts`
- **Base URL:** `https://api.cursor.com`
- **Official documentation:** [List Agent Artifacts](https://cursor.com/docs/cloud-agent/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the cloud agent whose artifacts should be listed. |

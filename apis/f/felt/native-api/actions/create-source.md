# Create Source with Felt

Creates a new data source in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/sources`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Source](https://developers.felt.com/rest-api/api-reference/sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Source name. |
| `connection` | body | `object` | yes | Source connection object matching the Felt source type contract. |
| `permissions` | body | `object` | no | Optional permissions object such as source_owner, workspace_editors, or project_editors. |

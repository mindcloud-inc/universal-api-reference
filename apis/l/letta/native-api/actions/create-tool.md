# Create Tool with Letta

Creates a new tool in Letta.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tools/`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Create Tool](https://docs.letta.com/api/resources/tools/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_code` | body | `string` | yes | The source code of the function to create as a Letta tool. |
| `description` | body | `string` | no | Optional description for the tool. |

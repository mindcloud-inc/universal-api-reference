# Update Tag with Sponsy

Updates a tag in Sponsy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/tags/:tagId`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Update Tag](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `list<string>` | yes | Tag ID from List Tags. |
| `text` | body | `string` | yes | Tag text. |
| `color` | body | `string` | yes | Tag hexadecimal color. |

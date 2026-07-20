# Create Tag with Sponsy

Creates a tag in Sponsy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tags`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Create Tag](https://docs.getsponsy.com/Workspace-Settings-10bb5594716880348de9ce02c29f53f0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Tag text. |
| `color` | body | `string` | yes | Tag hexadecimal color. |

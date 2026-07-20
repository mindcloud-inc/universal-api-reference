# Create Tag with Rebrandly

Creates a new tag in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Create Tag](https://developers.rebrandly.com/docs/creating-a-new-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique name of the tag. |
| `color` | body | `string` | no | Hexadecimal color assigned to the tag. |

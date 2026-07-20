# Create Tag with Teyuto

Creates a new tag in Teyuto.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Create Tag](https://docs.teyuto.com/api/create-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the tag. |
| `description` | body | `string` | yes | Description of the tag. |
| `privacy` | body | `string` | yes | Privacy of the content: hidden, public, or registered. |

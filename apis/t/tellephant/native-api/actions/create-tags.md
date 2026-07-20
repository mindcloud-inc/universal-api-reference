# Create tags with Tellephant

Creates tags for contacts in Tellephant.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/user/tags/create`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Create tags](https://app.tellephant.com/api-documentation#create-tags-on-platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of tag objects. Each item requires tag_name and may include tag_color. |

# Apply Tag with Zubie

Applies a tag in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/tag/{tag_key}/apply`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Apply Tag](https://developer.zubie.com/reference/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_keys[]` | body | `array<string>` | yes | Keys of entities to add or remove the tag from. |
| `tag_key` | path | `string` | yes | Unique tag key. |

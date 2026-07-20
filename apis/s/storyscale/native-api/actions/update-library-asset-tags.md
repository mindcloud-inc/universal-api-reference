# Update Library Asset Tags with Storyscale

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/library/update-tags/{id}`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Update Library Asset Tags](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Storyscale library asset ID. |
| `tags` | body | `list<string>` | no | Tags to apply to the library asset. |

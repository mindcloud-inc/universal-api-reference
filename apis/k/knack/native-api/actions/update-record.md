# Update Record with Knack

## Endpoint

- **Method:** `PUT`
- **Path:** `/objects/:object_key/records/:record_id`
- **Base URL:** `https://api.knack.com/v1`
- **Official documentation:** [Update Record](https://docs.knack.com/reference/object-based-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_key` | path | `string` | yes | Knack object key from the Builder URL, such as object_3. |
| `record_id` | path | `string` | yes | Knack record ID to update. |

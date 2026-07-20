# Delete Record with Knack

## Endpoint

- **Method:** `DELETE`
- **Path:** `/objects/:object_key/records/:record_id`
- **Base URL:** `https://api.knack.com/v1`
- **Official documentation:** [Delete Record](https://docs.knack.com/reference/object-based-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_key` | path | `string` | yes | Knack object key from the Builder URL, such as object_3. |
| `record_id` | path | `string` | yes | Knack record ID to delete. |

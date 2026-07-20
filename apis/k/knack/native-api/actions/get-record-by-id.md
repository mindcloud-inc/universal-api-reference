# Get Record By ID with Knack

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/:object_key/records/:record_id`
- **Base URL:** `https://api.knack.com/v1`
- **Official documentation:** [Get Record By ID](https://docs.knack.com/reference/retrieving-one-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_key` | path | `string` | yes | Knack object key from the Builder URL, such as object_3. |
| `record_id` | path | `string` | yes | Knack record ID to retrieve, such as 69b4423b3c1f982951ba5309. |

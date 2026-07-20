# Get Wire Transfer with Column

## Endpoint

- **Method:** `GET`
- **Path:** `/transfers/wire/:wire_transfer_id`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Get Wire Transfer](https://column.com/docs/api/#wire-transfer/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wire_transfer_id` | path | `string` | yes | ID of the wire transfer to retrieve. |
| `expand` | query | `string` | no | Repeatable expansion key for additional wire fields such as raw_message. |

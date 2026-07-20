# List Calls with Dialpad

Retrieves concluded call records from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/call`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Calls](https://developers.dialpad.com/reference/calllist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
| `include_anonymized` | query | `boolean` | no | If set to true, includes call records that have been anonymized. |
| `started_after` | query | `number` | no | Only includes calls that started more recently than the specified UTC millisecond timestamp. |
| `started_before` | query | `number` | no | Only includes calls that started prior to the specified UTC millisecond timestamp. |
| `target_id` | query | `number` | no | The ID of a target to filter against. |
| `target_type` | query | `string` | no | The target type associated with the target ID. |

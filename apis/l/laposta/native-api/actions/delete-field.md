# Delete Field with Laposta

Deletes an existing custom field from Laposta.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/field/:fieldId`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Delete Field](https://api.laposta.nl/doc/index.en.php#fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldId` | path | `string` | yes | The ID of the field to delete. |
| `list_id` | query | `string` | yes | The ID of the list that owns the field. |

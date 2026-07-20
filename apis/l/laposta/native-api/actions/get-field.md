# Get Field with Laposta

Retrieves a custom field from Laposta.

## Endpoint

- **Method:** `GET`
- **Path:** `/field/:fieldId`
- **Base URL:** `https://api.laposta.nl/v2`
- **Official documentation:** [Get Field](https://api.laposta.nl/doc/index.en.php#fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldId` | path | `string` | yes | The ID of the field to retrieve. |
| `list_id` | query | `string` | yes | The ID of the list that owns the field. |

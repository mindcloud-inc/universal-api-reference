# Get Form Field with Paperform

Retrieves a field from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/fields/:field_key`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [Get Form Field](https://paperform.readme.io/reference/getformfield)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes | Paperform form slug or numeric ID. |
| `field_key` | path | `list<string>` | yes | Paperform field key within the selected form. |

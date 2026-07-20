# List Form Fields with Paperform

Retrieves fields from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/fields`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [List Form Fields](https://paperform.readme.io/reference/listformfields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes | Paperform form slug or numeric ID. |

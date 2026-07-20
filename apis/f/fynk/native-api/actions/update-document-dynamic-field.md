# Update Document Dynamic Field with fynk

Updates a document dynamic field in fynk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document/dynamic-fields/:dynamicField`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Update Document Dynamic Field](https://app.fynk.com/v1/docs#/operations/v1.documents.dynamic-fields.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `dynamicField` | path | `string` | no | Dynamic field UUID. |
| `value` | body | `string` | no | Updated dynamic field value. |

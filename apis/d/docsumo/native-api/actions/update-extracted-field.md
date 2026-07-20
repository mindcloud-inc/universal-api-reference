# Update Extracted Field with Docsumo

Updates an extracted field value in a Docsumo document.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/pik/apikey/:doc_id/field/:field_id/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Update Extracted Field](https://support.docsumo.com/reference/update-a-fields-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id` | path | `string` | yes | Docsumo document ID. |
| `field_id` | path | `string` | yes | Docsumo field ID. |
| `value` | body | `string` | yes | Replacement value for the extracted field. |

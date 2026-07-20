# Update Form (Patch) with Typeform

## Endpoint

- **Method:** `PATCH`
- **Path:** `/forms/:formId`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Update Form (Patch)](https://www.typeform.com/developers/create/reference/update-form-patch/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `op` | body | `string` | no | Patch operation. |
| `path` | body | `string` | no | JSON pointer path for the patch. |
| `value` | body | `string` | no | Patch value. |

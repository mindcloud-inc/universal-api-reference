# Update Form with ByteForms

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/:formId`
- **Base URL:** `https://api.forms.bytesuite.io/`
- **Official documentation:** [Update Form](https://forms.bytesuite.io/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `body` | body | `string` | no |
| `formId` | path | `string` | no |
| `name` | body | `string` | no |
| `responses_visibility` | body | `string` | no |
| `status` | body | `string` | no |
| `workspace_id` | body | `string` | no |
| `body[]` | body | `array<object>` | no |
| `body[]` | body | `array<object>` | no |

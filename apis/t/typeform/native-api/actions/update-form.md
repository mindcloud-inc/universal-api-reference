# Update Form with Typeform

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Update Form](https://www.typeform.com/developers/create/reference/update-form/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | no | Form fields definition. |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `hidden` | body | `string` | no | Hidden fields configuration. |
| `logic` | body | `string` | no | Logic jumps configuration. |
| `settings` | body | `string` | no | Form settings. |
| `thankyou_screens` | body | `string` | no | Thank-you screens definition. |
| `theme` | body | `string` | no | Theme configuration. |
| `title` | body | `string` | no | Form title. |
| `type` | body | `string` | no | Form type. |
| `variables` | body | `string` | no | Form variables definition. |
| `welcome_screens` | body | `string` | no | Welcome screens definition. |
| `workspace` | body | `string` | no | Workspace association. |

# Update Form Translation with Typeform

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId/translations/:language`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Update Form Translation](https://www.typeform.com/developers/create/reference/update-form-translation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | no | Translated fields payload. |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `language` | path | `string` | yes | Language code. |
| `messages` | body | `string` | no | Translated messages payload. |
| `thankyou_screens` | body | `string` | no | Translated thank-you screens payload. |
| `welcome_screens` | body | `string` | no | Translated welcome screens payload. |

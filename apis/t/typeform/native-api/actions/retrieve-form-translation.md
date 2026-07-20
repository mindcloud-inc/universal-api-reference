# Retrieve Form Translation with Typeform

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/translations/:language`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Retrieve Form Translation](https://www.typeform.com/developers/create/reference/retrieve-form-translation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `language` | path | `string` | yes | Language code. |

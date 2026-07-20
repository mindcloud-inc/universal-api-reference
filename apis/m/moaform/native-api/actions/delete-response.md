# Delete Response with Moaform

Deletes a form response from Moaform.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/responses/:responseId`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [Delete Response](https://help.moaform.com/hc/en-us/articles/28407769469209-Deleting-Response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
| `response_id` | path | `string` | yes | Unique ID of the response. |

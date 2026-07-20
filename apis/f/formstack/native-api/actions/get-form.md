# Get Form with Formstack

Retrieves details for a form from Formstack.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Get Form](https://developers.formstack.com/reference/getformdetails-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The ID of the form. |
| `withFields` | query | `boolean` | no | Include form fields in the response. |

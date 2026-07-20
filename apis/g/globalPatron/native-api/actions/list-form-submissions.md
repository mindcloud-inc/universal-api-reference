# List Form Submissions with Global Patron

Lists form submissions in Global Patron.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/restricted/form/{formId}/submissions`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [List Form Submissions](https://www.globalpatron.com/developers/api/submissions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `include_form_definition` | query | `boolean` | no | Include form definition in the submissions response. |
| `date_from` | query | `date` | no | Start date for submission filtering. |
| `date_to` | query | `date` | no | End date for submission filtering. |
| `batch_size` | query | `number` | no | Number of submissions to return in a batch. |

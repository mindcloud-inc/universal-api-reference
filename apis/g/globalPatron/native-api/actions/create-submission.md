# Create Submission with Global Patron

Creates a form submission in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/{formId}/submission`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Create Submission](https://www.globalpatron.com/developers/api/submissions/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form receiving the submission. |
| `form_fields[]` | body | `array<object>` | yes | Submission field values array from the GlobalPatron form definition. |

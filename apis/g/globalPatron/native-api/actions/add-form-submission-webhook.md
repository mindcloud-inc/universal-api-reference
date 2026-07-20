# Add Form Submission Webhook with Global Patron

Adds a form submission webhook in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/submissionwebhook`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Add Form Submission Webhook](https://www.globalpatron.com/developers/api/webhooks/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `webhook_url` | body | `string` | yes | Destination URL that will receive submission webhook calls. |
| `webhook_name` | body | `string` | yes | Human-readable webhook name. |

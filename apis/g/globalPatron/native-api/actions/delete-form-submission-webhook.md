# Delete Form Submission Webhook with Global Patron

Deletes a form submission webhook from Global Patron.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/restricted/form/{formId}/submissionwebhook/{submissionWebhookId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Delete Form Submission Webhook](https://www.globalpatron.com/developers/api/webhooks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `submissionWebhookId` | path | `string` | yes | ID of the submission webhook to delete. |

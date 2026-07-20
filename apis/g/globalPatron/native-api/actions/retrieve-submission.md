# Retrieve Submission with Global Patron

Retrieves a form submission from Global Patron.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/restricted/form/{formId}/submission/{submissionId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Retrieve Submission](https://www.globalpatron.com/developers/api/submissions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `submissionId` | path | `string` | yes | ID of the submission. |

# Create Form Submission with Jotform

Creates a form submission in Jotform.

## Endpoint

- **Method:** `POST`
- **Path:** `/form/:formId/submissions`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [Create Form Submission](https://api.jotform.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Form ID |
| `submission` | body | `object` | yes | Submission payload keyed by question identifiers. |

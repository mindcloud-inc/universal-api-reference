# Get Form Submission with Paperform

Retrieves a submission from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/submissions/:id`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [Get Form Submission](https://paperform.readme.io/reference/getformsubmission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes | The Paperform form slug or numeric ID. |
| `id` | path | `string` | yes | The Paperform submission ID. |

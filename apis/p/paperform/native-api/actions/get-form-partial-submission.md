# Get Form Partial Submission with Paperform

Retrieves a partial submission from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/partial-submissions/:id`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [Get Form Partial Submission](https://paperform.readme.io/reference/getformpartialsubmission)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes |
| `id` | path | `string` | yes |

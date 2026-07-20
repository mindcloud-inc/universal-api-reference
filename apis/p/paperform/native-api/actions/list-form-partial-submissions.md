# List Form Partial Submissions with Paperform

Retrieves partial submissions from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/partial-submissions`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [List Form Partial Submissions](https://paperform.readme.io/reference/listformpartialsubmissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes |

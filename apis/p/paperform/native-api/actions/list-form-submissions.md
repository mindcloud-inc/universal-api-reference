# List Form Submissions with Paperform

Retrieves submissions from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/submissions`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [List Form Submissions](https://paperform.readme.io/reference/listformsubmissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes | The Paperform form slug or numeric ID. |

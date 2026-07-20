# List Submissions with OpnForm

Lists submissions for an OpnForm form.

## Endpoint

- **Method:** `GET`
- **Path:** `/open/forms/:id/submissions`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [List Submissions](https://docs.opnform.com/api-reference/submissions/list-submissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the form. |
| `search` | query | `string` | no | Optional text to search across submission values. |
| `status` | query | `string` | no | Optional submission status filter: completed, partial, or all. |

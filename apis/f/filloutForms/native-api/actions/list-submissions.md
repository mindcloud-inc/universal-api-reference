# List Submissions with Fillout Forms

Retrieves submissions for a Fillout form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/submissions`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [List Submissions](https://www.fillout.com/help/api-reference/get-all-submissions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID to list submissions for. |
| `status` | query | `string` | no | Filter submissions by completion status. |
| `afterDate` | query | `date` | no | Return submissions created after this date-time. |
| `beforeDate` | query | `date` | no | Return submissions created before this date-time. |
| `search` | query | `string` | no | Free-text search across submissions. |
| `includeEditLink` | query | `boolean` | no | Include edit links in response items. |
| `includePreview` | query | `boolean` | no | Whether to include a preview of the submission content. |

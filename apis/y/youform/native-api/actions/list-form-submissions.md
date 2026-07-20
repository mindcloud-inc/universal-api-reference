# List Form Submissions with Youform

Lists submissions for a form in Youform.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formSlug/submissions`
- **Base URL:** `https://app.youform.com/api`
- **Official documentation:** [List Form Submissions](https://youform.com/api-docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formSlug` | path | `string` | yes | Slug of the form whose submissions you want to list. |
| `is_complete` | query | `boolean` | no | Optional filter for completed vs partial submissions. Omit unless you explicitly need it. |
| `sort_by` | query | `string` | no | Field to sort submissions by, for example `created_at`. |
| `sort_by_order` | query | `string` | no | Sort direction for `sort_by`, for example `asc` or `desc`. |

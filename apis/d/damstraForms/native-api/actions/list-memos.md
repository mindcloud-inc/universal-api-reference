# List Memos with Damstra Forms

Retrieves memos from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/memos`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Memos](https://sammapi.docs.apiary.io/#reference/memos/memo-collection/get-a-list-of-memos)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_template_id` | query | `number` | no | Only return forms associate with the specified draft template. Note that there can be many published versions of a given template, so you need to use draft_template_id if you to get all forms for that template regardless of version. |
| `project_id` | query | `number` | no | Only return forms associate with the specified project. |
| `raised_from` | query | `string` | no | Return forms where date raised is greater than or equal to the specified date. |
| `raised_to` | query | `string` | no | Return forms where date raised is less than or equal to the specified date. |
| `status` | query | `string` | no | Statuses to include in returned results. You can combine statuses by separating them with "\|" (e.g. draft\|open, open\|closed, etc.) RFI type memos can have status "Awaiting Response" and "Response Received". They appear in the GUI, but in the API are both treated as “Sent”. Accepted values: `0`, `1`, `2`, `3`. Send multiple values as a string separated by `\|`. |
| `template_id` | query | `number` | no | Only return forms associate with the specified published version of a template. See also draft_template_id. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |

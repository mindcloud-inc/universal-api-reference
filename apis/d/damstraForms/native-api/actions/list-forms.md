# List Forms with Damstra Forms

Retrieves forms from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Forms](https://sammapi.docs.apiary.io/#reference/forms/form-collection/get-a-list-of-forms)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_template_id` | query | `number` | no | Only return forms associate with the specified draft template. Note that there can be many published versions of a given template, so you need to use draft_template_id if you to get all forms for that template regardless of version. |
| `fully_approved` | query | `boolean` | no | Only return forms where all approval sections have been approved (or where there are no approval sections) |
| `project_id` | query | `number` | no | Only return forms associate with the specified project. |
| `raised_from` | query | `string` | no | Return forms where date raised is greater than or equal to the specified date. |
| `raised_to` | query | `string` | no | Return forms where date raised is less than or equal to the specified date. |
| `status` | query | `string` | no | Statuses to include in returned results. You can combine statuses by separating them with "\|" (e.g. draft\|open, open\|closed, etc.) Accepted values: `0`, `1`, `2`, `3`. Send multiple values as a string separated by `\|`. |
| `template_id` | query | `number` | no | Only return forms associate with the specified published version of a template. See also draft_template_id. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |

# List Templates with Damstra Forms

Retrieves templates from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Templates](https://sammapi.docs.apiary.io/#reference/templates/template-collection/get-a-list-of-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_inactive` | query | `boolean` | no | Include inactive templates. |
| `type` | query | `string` | no | Return templates of the specified type(s). Accepted values: `0`, `1`, `2`, `3`. Send multiple values as a string separated by `\|`. |
| `template_type` | query | `string` | no | Return only templates of a certain type. 1 = General Memo, 2 = Issue Memo, 3 = RFI Memo, 4 = Action, 5 = Form. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |
| `project_id` | query | `string` | no | The unique id (numeric) or uuid (string) of the project. Its purpose is to return results that belongs to a specific project. |
| `show_managed` | query | `boolean` | no | Determines whether to include integrated templates in the response. |

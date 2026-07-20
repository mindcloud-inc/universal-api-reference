# List Forms with Kit

Lists forms in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Forms](https://developers.kit.com/api-reference/forms/list-forms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Filter forms by status. Accepted values: `active`, `all`, `inactive`. |
| `type` | query | `list` | no | Filter forms by type (embed or hosted). Accepted values: `embed`, `hosted`. |
| `after` | query | `string` | no | Return results after this cursor. |
| `before` | query | `string` | no | Return results before this cursor. |
| `include_total_count` | query | `boolean` | no | Include total_count in pagination metadata. |
| `per_page` | query | `number` | no | Number of results per page. |

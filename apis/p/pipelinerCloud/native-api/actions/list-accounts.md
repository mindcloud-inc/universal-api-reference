# List Accounts with Pipeliner Cloud

Retrieves accounts from Pipeliner Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/Accounts`
- **Base URL:** `{serviceUrl}/api/v100/rest/spaces/{spaceId}`
- **Official documentation:** [List Accounts](https://pipelinercrm.eu.apidog.com/accounts-list-3640460e0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include-deleted` | query | `boolean` | no | Include deleted Accounts in the results. |
| `expand` | query | `string` | no | Expand related entities by API field name, for example owner or sales_unit. |
| `load-only` | query | `string` | no | Comma-separated list of fields to include in the response. |

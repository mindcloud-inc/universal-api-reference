# List CRM Accounts with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/crm/v1/accounts`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List CRM Accounts](https://docs.merge.dev/crm/accounts/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |

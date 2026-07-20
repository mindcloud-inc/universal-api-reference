# Get CRM Account with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/crm/v1/accounts/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get CRM Account](https://docs.merge.dev/crm/accounts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |

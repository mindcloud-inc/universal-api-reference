# List Breached Identities with UpGuard

Retrieves breached identities from your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/breaches`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Breached Identities](https://cyber-risk.upguard.com/api/docs#operation/breached_identities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breach_id` | query | `string` | no | The breach ID to filter on |
| `page_token` | query | `string` | no | The page_token from a previous request, use this to get the next page of results. |
| `page_size` | query | `number` | no | The number of results to return per page. |
| `sort_by` | query | `string` | no | The value to sort the breached identities by. |
| `sort_desc` | query | `boolean` | no | Whether or not to sort the results in descending order. |

# List Domains with UpGuard

Retrieves domains from your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Domains](https://cyber-risk.upguard.com/api/docs#operation/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Retrieve active domains |
| `inactive` | query | `boolean` | no | Retrieve inactive domains |
| `labels` | query | `string<string>` | no | Filter result by the provided labels Send multiple values as a string separated by `,`. |
| `page_token` | query | `string` | no | The page_token from a previous request, use this to get the next page of results. |
| `page_size` | query | `number` | no | The number of results to return per page. |
| `sort_by` | query | `string` | no | The value to sort the domains by. |
| `sort_desc` | query | `boolean` | no | Whether or not to sort the results in descending order. |

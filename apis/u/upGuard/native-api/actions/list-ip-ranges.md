# List IP Ranges with UpGuard

Retrieves IP ranges from your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/ranges`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List IP Ranges](https://cyber-risk.upguard.com/api/docs#operation/ranges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labels` | query | `string<string>` | no | Filter result by the provided labels Send multiple values as a string separated by `,`. |
| `page_token` | query | `string` | no | The page_token from a previous request, use this to get the next page of results. |
| `page_size` | query | `number` | no | The number of results to return per page. |
| `sort_by` | query | `string` | no | The value to sort the IP ranges by. |
| `sort_desc` | query | `boolean` | no | Whether or not to sort the results in descending order. |

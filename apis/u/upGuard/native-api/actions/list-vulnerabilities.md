# List Vulnerabilities with UpGuard

Retrieves potential vulnerabilities from your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/vulnerabilities`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vulnerabilities](https://cyber-risk.upguard.com/api/docs#operation/org_vulnerabilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labels` | query | `string<string>` | no | A case-insensitive comma separated list of website labels to filter results by Send multiple values as a string separated by `,`. |
| `page_token` | query | `string` | no | The next page token from a previous response, use this to get the next page of results. |
| `page_size` | query | `number` | no | The number of results to return per page. |

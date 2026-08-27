# List Sales Orders with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder`
- **Base URL:** `{uRL}`
- **Official documentation:** [List Sales Orders](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$select` | query | `string` | no |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |

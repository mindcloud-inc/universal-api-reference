# List Groups with Databricks

Retrieves groups from the Databricks account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/Groups`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Groups](https://docs.databricks.com/api/account/accountgroups/list)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Query by which the results have to be filtered. Supported operators are equals(`eq`), contains(`co`), starts with(`sw`) and not equals(`ne`). Additionally, simple expressions can be formed using logical operators - `and` and `or`. The [SCIM RFC](https://tools.ietf.org/html/rfc7644#section-3.4.2.2) has more details but we currently only support simple expressions. |
| `attributes` | query | `string` | no | Comma-separated list of attributes to return in response. |
| `excludedAttributes` | query | `string` | no | Comma-separated list of attributes to exclude in response. |
| `startIndex` | query | `number` | no | Specifies the index of the first result. First item is number 1. |
| `count` | query | `number` | no | Desired number of results per page. Default is 10000. |
| `sortBy` | query | `string` | no | Attribute to sort the results. |
| `sortOrder` | query | `string` | no | The order to sort the results. |

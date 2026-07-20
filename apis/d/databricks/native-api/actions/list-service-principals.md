# List Service Principals with Databricks

Retrieves service principals from the Databricks account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/ServicePrincipals`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Service Principals](https://docs.databricks.com/api/account/accountserviceprincipals/list)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributes` | query | `string` | no | Comma-separated list of attributes to return in response. |
| `count` | query | `number` | no | Desired number of results per page. Default is 10000. |
| `excludedAttributes` | query | `string` | no | Comma-separated list of attributes to exclude in response. |
| `filter` | query | `string` | no | Query by which the results have to be filtered. Supported operators are equals(`eq`), contains(`co`), starts with(`sw`) and not equals(`ne`). Additionally, simple expressions can be formed using logical operators - `and` and `or`. The [SCIM RFC](https://tools.ietf.org/html/rfc7644#section-3.4.2.2) has more details but we currently only support simple expressions. |
| `sortBy` | query | `string` | no | Attribute to sort the results. |
| `sortOrder` | query | `string` | no | The order to sort the results. |
| `startIndex` | query | `number` | no | Specifies the index of the first result. First item is number 1. |

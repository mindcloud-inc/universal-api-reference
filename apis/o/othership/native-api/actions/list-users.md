# List Users with Othership

Retrieves user records from Othership SCIM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Users`
- **Base URL:** `https://hwms-api.othership.com/api/v1/azure/scim`
- **Official documentation:** [List Users](https://www.ietf.org/rfc/rfc7644)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | SCIM filter expression used to limit returned users. |
| `sortBy` | query | `string` | no | SCIM attribute used to sort returned users. |
| `sortOrder` | query | `string` | no | Sort direction for the SCIM list request. |
| `startIndex` | query | `number` | no | 1-based start position for paginated SCIM results. |
| `count` | query | `number` | no | Maximum number of SCIM results to return. |
| `attributes` | query | `string` | no | Comma-separated SCIM attributes to include in the response. |
| `excludedAttributes` | query | `string` | no | Comma-separated SCIM attributes to omit from the response. |

# List Blocked Visitors with GoSquared

Retrieves blocked visitors for a GoSquared site.

## Endpoint

- **Method:** `GET`
- **Path:** `account/v1/blocked/visitors`
- **Base URL:** `https://api.gosquared.com`
- **Official documentation:** [List Blocked Visitors](https://www.gosquared.com/docs/account/blocked/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presenter` | query | `string` | no | Modifies the response data structure. Accepted values: plain, tags, indexedTags. |

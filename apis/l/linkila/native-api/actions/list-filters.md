# List Filters with Linkila

Retrieves saved filters from Linkila.

## Endpoint

- **Method:** `GET`
- **Path:** `/filters`
- **Base URL:** `https://app.linkila.com/integrations/api/v1`
- **Official documentation:** [List Filters](https://app.linkila.com/integrations/api/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor for pagination. Use the cursor returned in pageInfo from a previous response. |

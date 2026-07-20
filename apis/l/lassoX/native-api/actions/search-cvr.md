# Search CVR with Lasso X

Finds CVR companies or people in Lasso X by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/cvr/search`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [Search CVR](https://docs.lassox.com/data-apis/cvr/#search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query. Supports names, CVR numbers, Lasso IDs, phone numbers, and documented filters. |

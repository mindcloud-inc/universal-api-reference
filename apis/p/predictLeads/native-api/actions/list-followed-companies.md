# List Followed Companies with PredictLeads

Retrieves followed companies from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/followings`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Followed Companies](https://docs.predictleads.com/api_endpoints/follow_companies/retrieve_followed_companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |

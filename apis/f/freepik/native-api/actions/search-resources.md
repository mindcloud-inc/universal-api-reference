# Search Resources with Freepik

Finds Freepik resources by search term and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/resources`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Search Resources](https://docs.freepik.com/api-reference/resources/get-all-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | no | Search term used to find Freepik resources. |
| `order` | query | `list` | no | Search result ordering. Freepik supports relevance or recent. Accepted values: `recent`, `relevance`. |
| `limit` | query | `number` | no | Maximum number of resources to return. |
| `page` | query | `number` | no | One-based results page to request. |

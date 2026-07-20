# Search ASO with AppFollow

Retrieves ASO search results from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/aso/search`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Search ASO](https://docs.api.appfollow.io/reference/aso_search_api_v2_aso_search_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Search term. |
| `country` | query | `string` | no | Country code. |
| `device` | query | `string` | no | Device type. |

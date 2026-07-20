# List Rankings with AppFollow

Retrieves app rankings from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/meta/rankings`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Rankings](https://docs.api.appfollow.io/reference/rankings_api_v2_meta_rankings_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `country` | query | `string` | no | Country code. |
| `device` | query | `string` | no | Device type. |
| `genre_id` | query | `string` | no | Genre ID. |
| `date` | query | `string` | no | Date. |

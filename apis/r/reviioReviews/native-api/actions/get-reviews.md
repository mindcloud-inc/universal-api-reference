# Get Reviews with Revi.io Reviews

Retrieves reviews from Revi.io Reviews.

## Endpoint

- **Method:** `GET`
- **Path:** `/reviews`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Get Reviews](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_id` | query | `string` | no | Return reviews with an id_comment greater than this value. |
| `to_id` | query | `string` | no | Return reviews with an id_comment lower than this value. |
| `from_date` | query | `string` | no | Return reviews after this date or datetime boundary. |
| `to_date` | query | `string` | no | Return reviews before this date or datetime boundary. |
| `equal_to_rating` | query | `number` | no | Return reviews with a rating equal to this value. |
| `greater_than_rating` | query | `number` | no | Return reviews with a rating greater than this value. |
| `id_product` | query | `string` | no | Filter reviews for a specific product id. |
| `id_store` | query | `string` | no | Marketplace store id or comma-separated store ids. |
| `limit` | query | `number` | no | Maximum number of reviews to return. |

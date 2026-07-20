# Set Date Expiration with Cutt.ly

Sets date-based expiration for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set Date Expiration](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `expireCond` | query | `string` | yes | Expiration date in YYYY-MM-DD format. |
| `expireRedirect` | query | `string` | yes | Destination URL after the expiration date. |
| `expireUnique` | query | `number` | no | Set to 1 to count only unique clicks, or 0 for all clicks. |

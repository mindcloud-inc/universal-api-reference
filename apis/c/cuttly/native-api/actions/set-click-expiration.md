# Set Click Expiration with Cutt.ly

Sets click-based expiration for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set Click Expiration](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `expireCond` | query | `number` | yes | Number of clicks before expiration triggers. |
| `expireRedirect` | query | `string` | yes | Destination URL after the click threshold is reached. |
| `expireUnique` | query | `number` | no | Set to 1 to count only unique clicks, or 0 for all clicks. |

# Set Mobile Redirect with Cutt.ly

Sets a mobile redirect for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set Mobile Redirect](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `mobile` | query | `string` | yes | One of redirect, android, ios, or windowsMobile. |
| `destination` | query | `string` | yes | Destination URL for the mobile redirect. |

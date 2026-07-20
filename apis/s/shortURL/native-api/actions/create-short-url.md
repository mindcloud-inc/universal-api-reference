# Create Short URL with Short URL

Creates a new short URL in Short URL.

## Endpoint

- **Method:** `GET`
- **Path:** `https://:baseDomain/api/wrapper_api.php`
- **Base URL:** `https://surl.link`
- **Official documentation:** [Create Short URL](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_createshorturl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseDomain` | path | `string` | yes | Short URL domain to use for this request. Accepted values: `0`, `1`, `2`, `3`. |
| `url` | query | `string` | yes | Destination URL to redirect to. |
| `custom_url` | query | `string` | no | Optional custom short URL code. |
| `msuser` | query | `string` | no | Optional creator identifier. |
| `surl_desc` | query | `string` | no | Optional short URL description. |
| `expiry_date` | query | `date` | no | Optional expiration date in YYYY-MM-DD format. |
| `password` | query | `string` | no | Optional access password. |
| `uses` | query | `number` | no | Optional maximum number of uses. |

# Update Short URL with Short URL

Updates an existing short URL in Short URL.

## Endpoint

- **Method:** `GET`
- **Path:** `https://:baseDomain/api/wrapper_api.php`
- **Base URL:** `https://surl.link`
- **Official documentation:** [Update Short URL](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_modifyshorturl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseDomain` | path | `string` | yes | Short URL domain to use for this request. Accepted values: `0`, `1`, `2`, `3`. |
| `short_url` | query | `string` | yes | Short URL code to update. |
| `url` | query | `string` | yes | Updated destination URL. |
| `surl_desc` | query | `string` | no | Optional updated description. |
| `expiry_date` | query | `date` | no | Optional expiration date in YYYY-MM-DD format. |
| `password` | query | `string` | no | Optional updated access password. |
| `uses` | query | `number` | no | Optional maximum number of uses. |

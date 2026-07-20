# Delete Short URL with Short URL

Deletes an existing short URL from Short URL.

## Endpoint

- **Method:** `GET`
- **Path:** `https://:baseDomain/api/wrapper_api.php`
- **Base URL:** `https://surl.link`
- **Official documentation:** [Delete Short URL](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_deleteshorturl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseDomain` | path | `string` | yes | Short URL domain to use for this request. Accepted values: `0`, `1`, `2`, `3`. |
| `short_url` | query | `string` | yes | Short URL code to delete. |

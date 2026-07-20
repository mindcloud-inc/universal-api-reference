# List Short URLs with Short URL

Retrieves short URLs from Short URL.

## Endpoint

- **Method:** `GET`
- **Path:** `https://:baseDomain/api/wrapper_api.php`
- **Base URL:** `https://surl.link`
- **Official documentation:** [List Short URLs](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_getallshorturls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseDomain` | path | `string` | yes | Short URL domain to use for this request. Accepted values: `0`, `1`, `2`, `3`. |
| `msuser` | query | `string` | no | Optional creator filter. |

# Short URL: Native API Reference

A consolidated summary of Short URL's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/shorturl/
- **API base URL:** `https://surl.link`

## Authentication

### Username and License Key

Authenticates Short URL App requests with the registered Username and License Key fields documented by Short URL App.

### Credentials

- **Username:** `username` · required · ShortURLApp username used as the user request parameter.

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/shorturl/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml` |

Responses from this API use XML.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Short URL](actions/create-short-url.md) | `GET https://:baseDomain/api/wrapper_api.php` | [docs](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_createshorturl) |
| [Delete Short URL](actions/delete-short-url.md) | `GET https://:baseDomain/api/wrapper_api.php` | [docs](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_deleteshorturl) |
| [Get Account Info](actions/get-account-info.md) | `GET https://:baseDomain/api/wrapper_api.php` | [docs](https://www.shorturlapp.com) |
| [List Short URLs](actions/list-short-urls.md) | `GET https://:baseDomain/api/wrapper_api.php` | [docs](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_getallshorturls) |
| [Update Short URL](actions/update-short-url.md) | `GET https://:baseDomain/api/wrapper_api.php` | [docs](https://learn.microsoft.com/en-us/connectors/shorturl/#shorturl_modifyshorturl) |

# <img src="https://images.mindcloud.co/apps/icons/favicon-learn-microsoft-com-48x48-1_1778082777266.png" alt="Short URL logo" width="28" height="28"> Short URL: Universal API

Create, list, update, and delete Short URL App links across the official Short URL domains.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shortURL/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.shorturlapp.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/shorturl/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/get-account-info?connectionId=$CONNECTION_ID&baseDomain=surl.link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET |  |

### Short Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Short URL](actions/create-short-url.md) | POST | Creates a new short URL in Short URL. |
| [Delete Short URL](actions/delete-short-url.md) | DELETE | Deletes an existing short URL from Short URL. |
| [List Short URLs](actions/list-short-urls.md) | GET | Retrieves short URLs from Short URL. |
| [Update Short URL](actions/update-short-url.md) | PUT | Updates an existing short URL in Short URL. |


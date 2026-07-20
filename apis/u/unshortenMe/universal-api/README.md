# Unshorten.Me: Universal API

Unshorten.Me resolves shortened links to their final destination URL.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unshortenMe/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://unshorten.me
- **Vendor API docs:** https://unshorten.me/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Unshorten URL](actions/unshorten-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unshortenMe/latest/actions/unshorten-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fbit.ly%2F3DKWm5t" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Url Resolution

| Action | Method | Description |
| --- | --- | --- |
| [Unshorten URL](actions/unshorten-url.md) | GET | Retrieves an unshortened destination URL from Unshorten.Me. |


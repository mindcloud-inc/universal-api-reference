# <img src="https://images.mindcloud.co/apps/icons/icon-horse_1777394568066.png" alt="Icon Horse logo" width="28" height="28"> Icon Horse: Universal API

Fetch and display website favicons with fallbacks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iconHorse/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://icon.horse/
- **Vendor API docs:** https://icon.horse/usage

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Icon](actions/get-icon.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon?connectionId=$CONNECTION_ID&hostname=github.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Icon

| Action | Method | Description |
| --- | --- | --- |
| [Get Icon](actions/get-icon.md) | GET | Retrieves a website icon from Icon Horse by hostname. |
| [Get Icon by Email](actions/get-icon-by-email.md) | GET | Retrieves a website icon from Icon Horse by email. |
| [Get Icon by URI](actions/get-icon-by-uri.md) | GET | Retrieves a website icon from Icon Horse by URI. |


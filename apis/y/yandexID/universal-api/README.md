# <img src="https://images.mindcloud.co/apps/icons/yandex-id_1775664091037.png" alt="Yandex ID logo" width="28" height="28"> Yandex ID: Universal API

Authorize users with Yandex accounts via OAuth 2.0 and read the authenticated user's Yandex ID profile data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yandexID/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yandex.com/
- **Vendor API docs:** https://yandex.com/dev/id/doc/en/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yandexID/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET |  |


# <img src="https://images.mindcloud.co/apps/icons/zenlogin-brand_1777585435392.png" alt="Zenlogin logo" width="28" height="28"> Zenlogin: Universal API

Zenlogin provides a suspicious-login detection API that checks login events using a user identity, email address, user agent, and IP address.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zenlogin/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zenlogin.co
- **Vendor API docs:** https://zenlogin.co/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Login Check](actions/create-login-check.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenlogin/latest/actions/create-login-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityKey": "usr12345",
  "identityEmailAddress": "name@example.com",
  "userAgent": "Mozilla/5.0",
  "ipAddress": "20.169.78.172"
}'
```

## Actions (1)

### Login Check

| Action | Method | Description |
| --- | --- | --- |
| [Create Login Check](actions/create-login-check.md) | POST |  |


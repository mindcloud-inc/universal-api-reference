# <img src="https://images.mindcloud.co/apps/icons/favicon-developers-tiktok-com-48x48_1777045332367.png" alt="TikTok Accounts logo" width="28" height="28"> TikTok Accounts: Universal API

Read TikTok account profile information for authenticated users through TikTok Login Kit and Display API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tikTokAccounts/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tiktok.com
- **Vendor API docs:** https://developers.tiktok.com/doc/tiktok-api-v2-get-user-info/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokAccounts/latest/actions/get-user-info?connectionId=$CONNECTION_ID&fields=open_id%2Cavatar_url%2Cdisplay_name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Tiktok User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves profile information for the authenticated user in TikTok. |


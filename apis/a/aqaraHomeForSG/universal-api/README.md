# <img src="https://images.mindcloud.co/apps/icons/aqara-home-for-us-1776374851211_1776430616860.png" alt="Aqara Home for SG logo" width="28" height="28"> Aqara Home for SG: Universal API

Connect Aqara Home for Singapore through the Aqara Open Platform using signed SG requests and Aqara account authorization artifacts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aqaraHomeForSG/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aqara.com/
- **Vendor API docs:** https://opendoc.aqara.com/en/docs/developmanual/apiIntroduction/APIUsageGuide.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Access Token](actions/get-access-token.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authCode": "string",
  "account": "string"
}'
```

## Actions (3)

### Access Reviews

| Action | Method | Description |
| --- | --- | --- |
| [Request Auth Code](actions/request-auth-code.md) | POST | Requests an authorization code from Aqara Home for SG. |

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST | Obtains an access token from Aqara Home for SG. |
| [Refresh Access Token](actions/refresh-access-token.md) | PUT | Refreshes access and refresh tokens in Aqara Home for SG. |


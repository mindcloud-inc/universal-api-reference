# NextDNS: Update Security Settings

Updates security settings for an existing NextDNS profile.

```
PUT https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/update-security-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/update-security-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/update-security-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `threatIntelligenceFeeds` | boolean | no | Enable threat intelligence feeds. |
| `aiThreatDetection` | boolean | no | Enable AI threat detection. |
| `googleSafeBrowsing` | boolean | no | Enable Google Safe Browsing protection. |
| `cryptojacking` | boolean | no | Block cryptojacking threats. |
| `dnsRebinding` | boolean | no | Block DNS rebinding attacks. |
| `idnHomographs` | boolean | no | Block IDN homograph attacks. |
| `typosquatting` | boolean | no | Block typosquatting domains. |
| `dga` | boolean | no | Block domain generation algorithm domains. |
| `nrd` | boolean | no | Block newly registered domains. |
| `ddns` | boolean | no | Block dynamic DNS domains. |
| `parking` | boolean | no | Block parking domains. |
| `csam` | boolean | no | Block CSAM-related domains. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NextDNS API returns.

## Native endpoint

Through the native NextDNS API, this operation is `PATCH /profiles/:profile/security` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-security-settings.md) for the provider-specific parameters and requirements.


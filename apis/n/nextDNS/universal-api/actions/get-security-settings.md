# NextDNS: Get Security Settings

Retrieves security settings for a NextDNS profile.

```
GET https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-security-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-security-settings?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-security-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiThreatDetection": true,
      "cryptojacking": true,
      "csam": true,
      "ddns": true,
      "dga": true,
      "dnsRebinding": true,
      "googleSafeBrowsing": true,
      "idnHomographs": true,
      "nrd": true,
      "parking": true,
      "threatIntelligenceFeeds": true,
      "tlds": [
        {}
      ],
      "typosquatting": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiThreatDetection` | boolean |  |
| `cryptojacking` | boolean |  |
| `csam` | boolean |  |
| `ddns` | boolean |  |
| `dga` | boolean |  |
| `dnsRebinding` | boolean |  |
| `googleSafeBrowsing` | boolean |  |
| `idnHomographs` | boolean |  |
| `nrd` | boolean |  |
| `parking` | boolean |  |
| `threatIntelligenceFeeds` | boolean |  |
| `tlds` | array<object> |  |
| `typosquatting` | boolean |  |

## Native endpoint

Through the native NextDNS API, this operation is `GET /profiles/:profile/security` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-security-settings.md) for the provider-specific parameters and requirements.


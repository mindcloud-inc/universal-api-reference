# Short.io: List Domains

Retrieves domains from Short.io.

```
GET https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-domains?${params}`, {
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
| `pattern` | string | no |  |
| `teamId` | number | no |  |
| `noTeamId` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caseSensitive": true,
      "clientStorage": {},
      "cloaking": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enableAI": true,
      "enableConversionTracking": true,
      "exportEnabled": true,
      "hasFavicon": true,
      "hideReferer": true,
      "hideVisitorIp": true,
      "hostname": "Ava Chen",
      "httpsLevel": "string",
      "httpsLinks": true,
      "id": 1,
      "incrementCounter": "string",
      "integrationAdroll": "string",
      "integrationFB": "string",
      "integrationGA": "string",
      "integrationGTM": "string",
      "isFavorite": true,
      "linkType": "https://example.com",
      "qrScanTracking": true,
      "robots": "string",
      "segmentKey": "string",
      "sslCertExpirationDate": "2026-05-07T12:00:00.000Z",
      "sslCertInstalledSuccess": true,
      "state": "string",
      "teamId": 1,
      "unicodeHostname": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhookURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caseSensitive` | boolean |  |
| `clientStorage` | object |  |
| `cloaking` | boolean |  |
| `createdAt` | date |  |
| `enableAI` | boolean |  |
| `enableConversionTracking` | boolean |  |
| `exportEnabled` | boolean |  |
| `hasFavicon` | boolean |  |
| `hideReferer` | boolean |  |
| `hideVisitorIp` | boolean |  |
| `hostname` | string |  |
| `httpsLevel` | string |  |
| `httpsLinks` | boolean |  |
| `id` | number |  |
| `incrementCounter` | string |  |
| `integrationAdroll` | string |  |
| `integrationFB` | string |  |
| `integrationGA` | string |  |
| `integrationGTM` | string |  |
| `isFavorite` | boolean |  |
| `linkType` | string |  |
| `qrScanTracking` | boolean |  |
| `robots` | string |  |
| `segmentKey` | string |  |
| `sslCertExpirationDate` | date |  |
| `sslCertInstalledSuccess` | boolean |  |
| `state` | string |  |
| `teamId` | number |  |
| `unicodeHostname` | string |  |
| `updatedAt` | date |  |
| `webhookURL` | string |  |

## Native endpoint

Through the native Short.io API, this operation is `GET /api/domains` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.


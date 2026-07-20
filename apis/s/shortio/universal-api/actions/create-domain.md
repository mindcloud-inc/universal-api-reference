# Short.io: Create Domain

Creates a new domain in Short.io.

```
POST https://connect.mindcloud.co/v1/universal/shortio/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortio/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostname` | string | yes |  |
| `hideReferer` | boolean | no |  |
| `linkType` | list<string> | no | One of: `eight-char`, `four-char`, `increment`, `random`, `secure`, `ten-char`. |

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
      "integrationTT": "string",
      "linkType": "https://example.com",
      "qrScanTracking": true,
      "robots": "string",
      "sslCertExpirationDate": "2026-05-07T12:00:00.000Z",
      "sslCertInstalledSuccess": true,
      "state": "string",
      "unicodeHostname": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caseSensitive` | boolean | Whether links are case sensitive. |
| `clientStorage` | object | Client-side storage configuration. |
| `cloaking` | boolean | Whether cloaking is enabled. |
| `createdAt` | date | Creation timestamp. |
| `enableAI` | boolean | Whether AI features are enabled. |
| `enableConversionTracking` | boolean | Whether conversion tracking is enabled. |
| `exportEnabled` | boolean | Whether exports are enabled. |
| `hasFavicon` | boolean | Whether a favicon is configured. |
| `hideReferer` | boolean | Whether the domain hides the referrer. |
| `hideVisitorIp` | boolean | Whether visitor IP addresses are hidden. |
| `hostname` | string | Domain hostname. |
| `httpsLevel` | string | HTTPS enforcement level. |
| `httpsLinks` | boolean | Whether HTTPS links are enabled. |
| `id` | number | Short.io domain identifier. |
| `incrementCounter` | string | Increment counter mode. |
| `integrationTT` | string | TikTok integration identifier when configured. |
| `linkType` | string | Default link type for the domain. |
| `qrScanTracking` | boolean | Whether QR scan tracking is enabled. |
| `robots` | string | Robots policy. |
| `sslCertExpirationDate` | date | SSL certificate expiration date. |
| `sslCertInstalledSuccess` | boolean | Whether SSL certificate installation succeeded. |
| `state` | string | Domain configuration state. |
| `unicodeHostname` | string | Unicode hostname representation. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | number | Owner user identifier. |

## Native endpoint

Through the native Short.io API, this operation is `POST /domains` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.


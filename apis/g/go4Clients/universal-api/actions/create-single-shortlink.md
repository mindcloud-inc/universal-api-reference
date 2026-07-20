# Go4Clients: Create Single Shortlink

Creates a shortlink without a campaign in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-single-shortlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-single-shortlink" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "mindcloud-api-shortlink",
  "expirationDays": "1",
  "type": "URL"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-single-shortlink', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "mindcloud-api-shortlink",
    "expirationDays": "1",
    "type": "URL"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | Shortlink key. Example: `mindcloud-api-shortlink`. |
| `expirationDays` | number | yes | How many days the shortlink remains active. Example: `1`. |
| `type` | string | yes | Shortlink target type: URL or LANDING. Example: `URL`. |
| `url` | string | no | Target URL when type is URL. Example: `https://www.google.com`. |
| `landingId` | string | no | Landing identifier when type is LANDING. Example: `landing-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "key": "string",
      "link": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Generated short code. |
| `key` | string | Key used to generate the shortlink. |
| `link` | string | Generated shortlink URL. |
| `url` | string | Destination URL for the shortlink. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/shortlink/v1.0/single` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-single-shortlink.md) for the provider-specific parameters and requirements.


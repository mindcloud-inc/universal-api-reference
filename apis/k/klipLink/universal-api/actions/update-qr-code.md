# KlipLink: Update QR Code



```
PUT https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KlipLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shortUrl` | string | yes | The short URL identifier, for example klipl.ink/example. |
| `destinationUrl` | string | no | Optional new destination URL for the QR code. |
| `title` | string | no | Optional new title for the QR code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KlipLink API returns.

## Native endpoint

Through the native KlipLink API, this operation is `PUT /v1/qrcodes/:short_url` (base URL `https://api.klipl.ink`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.


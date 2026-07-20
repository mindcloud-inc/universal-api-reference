# WhatsScale: Send Location

Sends a location message through WhatsScale.

```
POST https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "latitude": 1,
  "longitude": 1,
  "session": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/send-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "latitude": 1,
    "longitude": 1,
    "session": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | Recipient chat ID. |
| `latitude` | number | yes | Latitude from -90 to 90. |
| `longitude` | number | yes | Longitude from -180 to 180. |
| `session` | string | yes | Session name from /api/sessions. |
| `title` | string | no | Optional label for the location pin. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native WhatsScale API, this operation is `POST /api/sendLocation` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-location.md) for the provider-specific parameters and requirements.


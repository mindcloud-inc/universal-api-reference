# Vestaboard: Send Message

Sends a new message to Vestaboard.

```
POST https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vestaboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no | Plain-text message to show on the Vestaboard. |
| `characters[]` | array<array> | no | Two-dimensional array of Vestaboard character codes. |
| `forced` | boolean | no | Override quiet hours when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Unix timestamp in milliseconds when the message was created. |
| `id` | string | Identifier of the created message. |
| `status` | string | Vestaboard API status string. |

## Native endpoint

Through the native Vestaboard API, this operation is `POST /` (base URL `https://cloud.vestaboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.


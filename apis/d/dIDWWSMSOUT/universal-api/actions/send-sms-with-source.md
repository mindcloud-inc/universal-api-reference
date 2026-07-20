# DIDWW SMS OUT: Send SMS With Source

Creates an outbound SMS in DIDWW SMS OUT with a source DID.

```
POST https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-sms-with-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DIDWW SMS OUT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-sms-with-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string",
  "source": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-sms-with-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string",
    "source": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | Recipient number in E.164 format. |
| `source` | string | yes | Sender DID in E.164 format. |
| `content` | string | yes | SMS body text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string | Created outbound message identifier. |
| `data.type` | string | JSON:API resource type. |

## Native endpoint

Through the native DIDWW SMS OUT API, this operation is `POST /outbound_messages` (base URL `https://us.sms-out.didww.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-with-source.md) for the provider-specific parameters and requirements.


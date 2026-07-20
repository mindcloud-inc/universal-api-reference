# TextingHouse: Send Service SMS

Creates a service SMS in TextingHouse.

```
POST https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-service-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TextingHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-service-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "33628000000",
  "txt": "Order 1845 is ready for pickup."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-service-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "33628000000",
    "txt": "Order 1845 is ready for pickup."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient phone number in international format, including country code. Example: `33628000000`. |
| `txt` | string | yes | SMS content to send. Example: `Order 1845 is ready for pickup.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `climsgid` | string | no | Optional client-defined message identifier, up to 32 characters. Example: `FRS78913246`. |
| `from` | string | no | Optional sender ID approved on your TextingHouse account. Example: `MindCloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiMessageId": "string",
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiMessageId` | string | TextingHouse API message ID returned after a successful send. |
| `rawResponse` | string | Plain-text response returned by TextingHouse. |

## Native endpoint

Through the native TextingHouse API, this operation is `POST /do` (base URL `https://api.textinghouse.com/http/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-service-sms.md) for the provider-specific parameters and requirements.


# TextingHouse: Send Test SMS To 999

Creates a test SMS to 999 in TextingHouse.

```
POST https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-test-sms-to999
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TextingHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-test-sms-to999" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "txt": "MindCloud health check"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/send-test-sms-to999', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "txt": "MindCloud health check"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `txt` | string | yes | SMS content to send to the TextingHouse test number. Example: `MindCloud health check`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `climsgid` | string | no | Optional client-defined message identifier, up to 32 characters. Example: `TEST-20260402`. |

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

Through the native TextingHouse API, this operation is `POST /do` (base URL `https://api.textinghouse.com/http/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-test-sms-to999.md) for the provider-specific parameters and requirements.


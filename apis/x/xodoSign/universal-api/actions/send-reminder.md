# Xodo Sign: Send Reminder

Sends a reminder to a document signer in Xodo Sign.

```
PUT https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/send-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/send-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string",
  "document_hash": "string",
  "signer_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/send-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string",
    "document_hash": "string",
    "signer_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_id` | string | yes | Business ID to scope the reminder request. |
| `document_hash` | string | yes | Unique document hash to send a reminder for. |
| `signer_id` | string | yes | Signer ID that should receive the reminder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the reminder request succeeded. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /send_reminder` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reminder.md) for the provider-specific parameters and requirements.


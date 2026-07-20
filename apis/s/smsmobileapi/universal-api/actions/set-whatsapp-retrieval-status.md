# Smsmobileapi: Set WhatsApp Retrieval Status

Updates WhatsApp retrieval status in Smsmobileapi.

```
PUT https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/set-whatsapp-retrieval-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smsmobileapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/set-whatsapp-retrieval-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statut": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/set-whatsapp-retrieval-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statut": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statut` | list | yes | Set WhatsApp retrieval to activated or deactivated explicitly. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "read_message_active": 1,
      "status_note": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `read_message_active` | number | Current WhatsApp retrieval state returned by the provider (1 active, 0 inactive). |
| `status_note` | string | Provider status label for the current retrieval state. |
| `success` | boolean | Whether the WhatsApp retrieval status update succeeded. |

## Native endpoint

Through the native Smsmobileapi API, this operation is `GET /getwa/active/` (base URL `https://api.smsmobileapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-whatsapp-retrieval-status.md) for the provider-specific parameters and requirements.


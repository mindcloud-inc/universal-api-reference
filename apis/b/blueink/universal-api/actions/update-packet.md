# Blueink: Update Packet

Updates an existing packet in Blueink.

```
PUT https://connect.mindcloud.co/v1/universal/blueink/latest/actions/update-packet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/update-packet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueink/latest/actions/update-packet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packetId` | string | yes | Packet ID to update. |
| `name` | string | no | Updated signer name. |
| `suppressReminder` | boolean | no | Whether to suppress reminder notifications for this signer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authId": true,
      "authSelfie": true,
      "authSms": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "deliverVia": "string",
      "email": "ava@example.com",
      "id": "string",
      "key": "string",
      "lastAccessedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "order": 1,
      "personId": "string",
      "phone": "string",
      "signingCompleteRedirect": "string",
      "status": "string",
      "suppressAll": true,
      "suppressDocsReady": true,
      "suppressReminder": true,
      "suppressSigning": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authId` | boolean |  |
| `authSelfie` | boolean |  |
| `authSms` | boolean |  |
| `completedAt` | date |  |
| `deliverVia` | string |  |
| `email` | string |  |
| `id` | string |  |
| `key` | string |  |
| `lastAccessedAt` | date |  |
| `name` | string |  |
| `order` | number |  |
| `personId` | string |  |
| `phone` | string |  |
| `signingCompleteRedirect` | string |  |
| `status` | string |  |
| `suppressAll` | boolean |  |
| `suppressDocsReady` | boolean |  |
| `suppressReminder` | boolean |  |
| `suppressSigning` | boolean |  |

## Native endpoint

Through the native Blueink API, this operation is `PATCH /packets/:packetId/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-packet.md) for the provider-specific parameters and requirements.


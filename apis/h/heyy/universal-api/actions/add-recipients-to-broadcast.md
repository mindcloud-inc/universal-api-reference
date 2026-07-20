# Heyy: Add Recipients To Broadcast

Adds recipients to a broadcast in Heyy.

```
PUT https://connect.mindcloud.co/v1/universal/heyy/latest/actions/add-recipients-to-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/add-recipients-to-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcastId": "string",
  "channelId": "string",
  "contactsIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/add-recipients-to-broadcast', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcastId": "string",
    "channelId": "string",
    "contactsIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcastId` | string | yes | The Heyy broadcast ID. |
| `channelId` | string | yes | The Heyy channel ID. |
| `contactsIds[]` | array<string> | yes | The contact IDs to add as recipients. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "phoneNumber": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `POST /[:channelId]/broadcasts/:broadcastId/recipients` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-recipients-to-broadcast.md) for the provider-specific parameters and requirements.


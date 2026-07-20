# Heyy: List Broadcast Recipients

Retrieves broadcast recipients from a Heyy channel.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-broadcast-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-broadcast-recipients?connectionId=$CONNECTION_ID&broadcastId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcastId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-broadcast-recipients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcastId` | string | yes | The Heyy broadcast ID. |
| `channelId` | string | yes | The Heyy channel ID. |

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

Through the native Heyy API, this operation is `GET /[:channelId]/broadcasts/:broadcastId/recipients` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-broadcast-recipients.md) for the provider-specific parameters and requirements.


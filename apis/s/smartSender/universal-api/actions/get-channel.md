# Smart Sender: Get Channel

Retrieves a channel from Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/get-channel?${params}`, {
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
| `channelId` | string | yes | The Smart Sender channel ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "app": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "occupied": true,
      "referrer": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `app` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `link` | string |  |
| `name` | string |  |
| `occupied` | boolean |  |
| `referrer` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/channels/:channelId` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.


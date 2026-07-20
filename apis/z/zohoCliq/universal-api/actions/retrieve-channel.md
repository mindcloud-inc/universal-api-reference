# Zoho Cliq: Retrieve Channel

Retrieves a channel from Zoho Cliq by ID.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-channel?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/retrieve-channel?${params}`, {
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
| `channelId` | string | yes | The ID of the channel to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel_id": "string",
      "chat_id": "string",
      "creation_time": "string",
      "description": "string",
      "invite_only": true,
      "joined": true,
      "last_modified_time": "string",
      "level": "string",
      "name": "Ava Chen",
      "participant_count": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_id` | string |  |
| `chat_id` | string |  |
| `creation_time` | string |  |
| `description` | string |  |
| `invite_only` | boolean |  |
| `joined` | boolean |  |
| `last_modified_time` | string |  |
| `level` | string |  |
| `name` | string |  |
| `participant_count` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /channels/:channelId` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-channel.md) for the provider-specific parameters and requirements.


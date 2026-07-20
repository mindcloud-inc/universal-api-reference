# Landbot: List Channels

Retrieves channels from Landbot.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-channels?${params}`, {
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
| `type` | string | no | Filter channels by type. |
| `active` | boolean | no | Filter channels by active status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "chats": 1,
      "createdAt": 1,
      "hooks": [
        "string"
      ],
      "hsm": 1,
      "id": 1,
      "name": "Ava Chen",
      "token": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `chats` | number |  |
| `createdAt` | number |  |
| `hooks[]` | string |  |
| `hsm` | number |  |
| `id` | number |  |
| `name` | string |  |
| `token` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/channels/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.


# Twist: Get Channel

Retrieves a channel from Twist by ID.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-channel?${params}`, {
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
| `channelId` | number | yes | The id of the channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "color": 1,
      "createdTs": 1,
      "creator": 1,
      "description": "string",
      "filters": {
        "filterClosed": "string"
      },
      "icon": 1,
      "id": 1,
      "isFavorited": true,
      "name": "Ava Chen",
      "public": true,
      "useDefaultRecipients": true,
      "userIds": [
        1
      ],
      "version": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `color` | number |  |
| `createdTs` | number |  |
| `creator` | number |  |
| `description` | string |  |
| `filters.filterClosed` | string |  |
| `icon` | number |  |
| `id` | number |  |
| `isFavorited` | boolean |  |
| `name` | string |  |
| `public` | boolean |  |
| `useDefaultRecipients` | boolean |  |
| `userIds[]` | number |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Twist API, this operation is `GET /channels/getone` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.


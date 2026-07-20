# Twist: Update Channel

Updates an existing channel in Twist.

```
PUT https://connect.mindcloud.co/v1/universal/twist/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twist/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | number | yes | The id of the channel. |
| `description` | string | no | The description of the channel. |
| `name` | string | yes | The name of the channel. |
| `public` | boolean | no | If enabled, the channel will be marked as public. |

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

Through the native Twist API, this operation is `POST /channels/update` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.


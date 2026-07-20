# Pushpad: Create Project

Creates a new project in Pushpad.

```
POST https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "senderId": 1,
  "website": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "senderId": 1,
    "website": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badgeUrl` | string | no |  |
| `iconUrl` | string | no |  |
| `name` | string | yes |  |
| `notificationsRequireInteraction` | boolean | no |  |
| `notificationsSilent` | boolean | no |  |
| `notificationsTtl` | number | no |  |
| `senderId` | number | yes |  |
| `website` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeUrl": "https://example.com",
      "createdAt": "string",
      "iconUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "notificationsRequireInteraction": true,
      "notificationsSilent": true,
      "notificationsTtl": 1,
      "senderId": 1,
      "subscriptionsCount": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeUrl` | string |  |
| `createdAt` | string |  |
| `iconUrl` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notificationsRequireInteraction` | boolean |  |
| `notificationsSilent` | boolean |  |
| `notificationsTtl` | number |  |
| `senderId` | number |  |
| `subscriptionsCount` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Pushpad API, this operation is `POST /projects` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.


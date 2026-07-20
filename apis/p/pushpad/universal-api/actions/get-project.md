# Pushpad: Get Project

Retrieves a specific project from Pushpad.

```
GET https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-project?${params}`, {
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
| `projectId` | number | yes |  |

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

Through the native Pushpad API, this operation is `GET /projects/:project_id` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.


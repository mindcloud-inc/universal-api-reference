# Pushpad: List Projects

Retrieves all projects available in Pushpad.

```
GET https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "url": "https://example.com",
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
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Pushpad API, this operation is `GET /projects` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.


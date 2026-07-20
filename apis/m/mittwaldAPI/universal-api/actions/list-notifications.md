# mittwald: List Notifications

Retrieves unread notifications from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-notifications?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "read": true,
      "severity": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `read` | boolean |  |
| `severity` | string |  |
| `type` | string |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/notifications` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.


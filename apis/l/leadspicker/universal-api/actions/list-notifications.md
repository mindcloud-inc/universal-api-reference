# Leadspicker: List Notifications

Retrieves notifications from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-notifications?${params}`, {
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
| `limit` | number | no | Maximum notifications to return. Default: `10`. |
| `offset` | number | no | Number of notifications to skip. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notifications": [
        {}
      ],
      "unread_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notifications` | array<object> |  |
| `unread_count` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/notifications` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.


# Next Cloud OCS: List Notifications

Retrieves notifications from Next Cloud OCS.

```
GET https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/list-notifications?${params}`, {
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
      "app": "string",
      "data": [
        {}
      ],
      "datetime": "string",
      "message": "string",
      "notification_id": "string",
      "ocs": {},
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | string |  |
| `data` | array<object> |  |
| `datetime` | string |  |
| `message` | string |  |
| `notification_id` | string |  |
| `ocs` | object |  |
| `subject` | string |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `GET /ocs/v2.php/apps/notifications/api/v2/notifications` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.


# PushAlert: Delete Scheduled Notification



```
DELETE https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/delete-scheduled-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/delete-scheduled-notification?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/delete-scheduled-notification?${params}`, {
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
| `id` | string | yes | PushAlert scheduled notification ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Provider message returned for the delete request. |
| `success` | boolean | Whether the scheduled notification delete request succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `POST /rest/v2/web-push/delete/:id` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scheduled-notification.md) for the provider-specific parameters and requirements.


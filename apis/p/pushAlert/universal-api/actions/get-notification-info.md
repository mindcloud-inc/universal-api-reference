# PushAlert: Get Notification Info



```
GET https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-notification-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-notification-info?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-notification-info?${params}`, {
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
| `id` | string | yes | PushAlert notification ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempted": "string",
      "clicked": "string",
      "ctr": "string",
      "delivered": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempted` | string | Total subscribers attempted as returned by PushAlert. |
| `clicked` | string | Total clicks as returned by PushAlert. |
| `ctr` | string | Click-through rate as returned by PushAlert. |
| `delivered` | string | Total notifications delivered as returned by PushAlert. |
| `success` | boolean | Whether the notification stats request succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `GET /rest/v2/web-push/info/:id` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-info.md) for the provider-specific parameters and requirements.


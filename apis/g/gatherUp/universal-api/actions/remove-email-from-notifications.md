# GatherUp: Remove Email from Notifications

Deletes a notification email from GatherUp.

```
DELETE https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/remove-email-from-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/remove-email-from-notifications?connectionId=$CONNECTION_ID&businessId=1&email=ava%40example.com&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "1",
  "email": "ava@example.com",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/remove-email-from-notifications?${params}`, {
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
| `businessId` | number | yes | Business id. |
| `email` | string | yes | Email address. |
| `type` | string | yes | Notification type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/notifications/email/remove` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-email-from-notifications.md) for the provider-specific parameters and requirements.


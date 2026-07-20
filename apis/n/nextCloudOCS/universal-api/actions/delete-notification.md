# Next Cloud OCS: Delete Notification

Deletes a notification from Next Cloud OCS.

```
DELETE https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/delete-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/delete-notification?connectionId=$CONNECTION_ID&notificationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/delete-notification?${params}`, {
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
| `notificationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "ocs": {},
      "status": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `ocs` | object |  |
| `status` | string |  |
| `statuscode` | number |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `DELETE /ocs/v2.php/apps/notifications/api/v2/notifications/{{notificationId}}` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-notification.md) for the provider-specific parameters and requirements.


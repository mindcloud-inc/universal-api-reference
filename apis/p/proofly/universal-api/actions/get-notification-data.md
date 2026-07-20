# Proofly: Get Notification Data

Retrieves notification data from your Proofly account.

```
GET https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-notification-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-notification-data?connectionId=$CONNECTION_ID&notificationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-notification-data?${params}`, {
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
| `notificationId` | string | yes | The notification ID from Get Campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "date": "2026-05-07T12:00:00.000Z",
      "ip": "string",
      "location": {},
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Notification payload data |
| `date` | date | Event timestamp |
| `ip` | string | Source IP address |
| `location` | object | Source location |
| `type` | string | Notification event type |
| `url` | string | Source URL |

## Native endpoint

Through the native Proofly API, this operation is `GET /data/:notificationId` (base URL `https://proofly.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-data.md) for the provider-specific parameters and requirements.


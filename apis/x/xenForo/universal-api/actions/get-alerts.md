# XenForo: Get Alerts

Retrieves a list of user alerts from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-alerts?${params}`, {
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
| `unread` | boolean | no | If true, gets only unread alerts. |
| `unviewed` | boolean | no | If true, gets only unviewed alerts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": [
        {
          "alert_id": 1,
          "alert_text": "string",
          "alert_url": "https://example.com",
          "alerted_user_id": 1,
          "content_id": 1,
          "content_type": "string",
          "read_date": 1,
          "view_date": 1
        }
      ],
      "pagination": {
        "current_page": 1,
        "last_page": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts` | array<object> |  |
| `alerts[].alert_id` | number |  |
| `alerts[].alert_text` | string |  |
| `alerts[].alert_url` | string |  |
| `alerts[].alerted_user_id` | number |  |
| `alerts[].content_id` | number |  |
| `alerts[].content_type` | string |  |
| `alerts[].read_date` | number |  |
| `alerts[].view_date` | number |  |
| `pagination.current_page` | number |  |
| `pagination.last_page` | number |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /alerts/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alerts.md) for the provider-specific parameters and requirements.


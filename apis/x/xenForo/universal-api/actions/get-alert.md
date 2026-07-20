# XenForo: Get Alert

Retrieves the specified alert from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-alert?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-alert?${params}`, {
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
| `id` | number | yes | ID of the alert to retrieve. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert": {
        "alert_id": 1,
        "alert_text": "string",
        "alert_url": "https://example.com",
        "alerted_user_id": 1,
        "content_id": 1,
        "content_type": "string",
        "read_date": 1,
        "view_date": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert.alert_id` | number |  |
| `alert.alert_text` | string |  |
| `alert.alert_url` | string |  |
| `alert.alerted_user_id` | number |  |
| `alert.content_id` | number |  |
| `alert.content_type` | string |  |
| `alert.read_date` | number |  |
| `alert.view_date` | number |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /alerts/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert.md) for the provider-specific parameters and requirements.


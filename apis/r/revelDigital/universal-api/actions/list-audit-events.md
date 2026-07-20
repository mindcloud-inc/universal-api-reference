# Revel Digital: List Audit Events



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-audit-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-audit-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-audit-events?${params}`, {
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
      "account_id": "string",
      "action_name": "Ava Chen",
      "app_id": "string",
      "controller_name": "Ava Chen",
      "duration": "string",
      "event_id": 1,
      "event_type": "string",
      "geo_location": "string",
      "http_method": "string",
      "ip_address": "string",
      "remote_ip_address": "string",
      "response_code": "string",
      "timestamp": "string",
      "user_agent": "string",
      "user_id": "string",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `action_name` | string |  |
| `app_id` | string |  |
| `controller_name` | string |  |
| `duration` | string |  |
| `event_id` | number |  |
| `event_type` | string |  |
| `geo_location` | string |  |
| `http_method` | string |  |
| `ip_address` | string |  |
| `remote_ip_address` | string |  |
| `response_code` | string |  |
| `timestamp` | string |  |
| `user_agent` | string |  |
| `user_id` | string |  |
| `user_name` | string |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /account/auditevents` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audit-events.md) for the provider-specific parameters and requirements.


# Revel Digital: List Alerts



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-alerts?${params}`, {
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
      "alert_rule": {},
      "created_on": "string",
      "devices": [
        {}
      ],
      "id": "string",
      "is_active": true,
      "resolved_on": "string",
      "snoozed_until": "string",
      "updated_on": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_rule` | object |  |
| `created_on` | string |  |
| `devices` | array<object> |  |
| `id` | string |  |
| `is_active` | boolean |  |
| `resolved_on` | string |  |
| `snoozed_until` | string |  |
| `updated_on` | string |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /alerts` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.


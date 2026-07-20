# Kadoa: List Notification Settings



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-notification-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-notification-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-notification-settings?${params}`, {
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
| `workflowId` | string | no | Filter by workflow ID |
| `eventType` | string | no | Filter by event type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "settings": [
          {}
        ]
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.settings` | array<object> |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Kadoa API, this operation is `GET /v5/notifications/settings` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notification-settings.md) for the provider-specific parameters and requirements.


# Rachio Smart Hose Timer: List Webhook Event Types

Retrieves webhook event types from Rachio.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-webhook-event-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-webhook-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-webhook-event-types?${params}`, {
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
      "eventTypes": [
        "string"
      ],
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventTypes` | array<string> | Webhook event types available for the resource type. |
| `resourceType` | string | Resource type supported by the webhook service. |

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET https://cloud-rest.rach.io/webhook/listWebhookEventTypes` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-event-types.md) for the provider-specific parameters and requirements.


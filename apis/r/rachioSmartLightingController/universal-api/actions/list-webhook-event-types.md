# Rachio Smart Lighting Controller: List Webhook Event Types



```
GET https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-webhook-event-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Lighting Controller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-webhook-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-webhook-event-types?${params}`, {
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
| `eventTypes` | array<string> |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Rachio Smart Lighting Controller API, this operation is `GET https://cloud-rest.rach.io/webhook/listWebhookEventTypes` (base URL `https://cloud-rest.rach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-event-types.md) for the provider-specific parameters and requirements.


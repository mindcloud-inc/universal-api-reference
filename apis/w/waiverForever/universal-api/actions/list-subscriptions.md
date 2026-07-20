# WaiverForever: List Subscriptions

Retrieves webhook subscriptions from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-subscriptions?${params}`, {
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
      "createdBy": "string",
      "disabled": true,
      "event": "string",
      "id": "string",
      "secretKey": "string",
      "state": "string",
      "targetUrl": "https://example.com",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Actor that created the subscription. |
| `disabled` | boolean | Whether the subscription is disabled. |
| `event` | string | Subscribed event name. |
| `id` | string | Webhook subscription identifier. |
| `secretKey` | string | Secret key used to sign webhook payloads. |
| `state` | string | Provider state string for the subscription. |
| `targetUrl` | string | Webhook callback URL. |
| `templateId` | string | Template attached to the subscription. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v1/webhooks/` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.


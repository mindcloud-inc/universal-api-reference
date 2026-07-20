# CheckFlow: List Webhook Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-webhook-subscriptions?${params}`, {
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
| `source` | string | no | Filters by the source of the webhook. Defaults to ALL. Example: `ALL`. |
| `eventType` | string | no | Filters by event type. Defaults to ALL. Example: `ALL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "string",
      "eventType": "string",
      "id": "string",
      "isActive": true,
      "source": "string",
      "targetURL": "https://example.com",
      "taskContentKey": "string",
      "taskKey": "string",
      "teamID": 1,
      "templateKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | string | The timestamp when the subscription was created. |
| `eventType` | string | The event that triggers the subscription. |
| `id` | string | The subscription ID. |
| `isActive` | boolean | Whether the subscription is currently active. |
| `source` | string | The source label for the subscription. |
| `targetURL` | string | The destination URL that receives webhook events. |
| `taskContentKey` | string | The targeted task content key, or the zero GUID when not applicable. |
| `taskKey` | string | The targeted task key, or the zero GUID when not applicable. |
| `teamID` | number | The numeric team ID that owns the subscription. |
| `templateKey` | string | The targeted template key, or the zero GUID when not applicable. |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/web-hook/subscriptions` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.


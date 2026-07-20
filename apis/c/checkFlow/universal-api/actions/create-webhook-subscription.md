# CheckFlow: Create Webhook Subscription



```
POST https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "custom",
  "eventType": "task_completed",
  "targetUrl": "https://example.com/hooks/task-done"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "custom",
    "eventType": "task_completed",
    "targetUrl": "https://example.com/hooks/task-done"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | A label identifying the source of this subscription, such as custom or zapier. Example: `custom`. |
| `eventType` | string | yes | The event that triggers the webhook. Example: `task_completed`. |
| `targetUrl` | string | yes | The URL that CheckFlow will POST event data to. Example: `https://example.com/hooks/task-done`. |
| `templateKey` | string | no | Required when eventType is new_checklist. Example: `b90dd809-eefc-447e-8c17-5f0ca96df701`. |
| `taskKey` | string | no | Required when eventType is task_completed. Example: `07072bc4-f1eb-4536-819a-1ddb7dc109a1`. |
| `taskContentKey` | string | no | Required when eventType is file_uploaded. Example: `50d58518-e049-4474-84c7-036236e52923`. |

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
| `createdDateTime` | string | The ISO timestamp when the subscription was created. |
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

Through the native CheckFlow API, this operation is `POST /api/web-hook/subscribe` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.


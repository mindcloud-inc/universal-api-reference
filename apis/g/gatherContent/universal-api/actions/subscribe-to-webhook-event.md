# GatherContent: Subscribe To Webhook Event

Subscribes a webhook to an event in GatherContent.

```
POST https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/subscribe-to-webhook-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/subscribe-to-webhook-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_name": "Ava Chen",
  "project_id": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/subscribe-to-webhook-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_name": "Ava Chen",
    "project_id": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_name` | string | yes | Webhook event name. |
| `project_id` | string | yes | Project id. |
| `url` | string | yes | Webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_name": "Ava Chen",
      "id": "string",
      "project_id": 1,
      "source": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_name` | string |  |
| `id` | string |  |
| `project_id` | number |  |
| `source` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GatherContent API, this operation is `POST /projects/:project_id/webhooks/:event_name` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-webhook-event.md) for the provider-specific parameters and requirements.


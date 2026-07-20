# Perfit: Send Custom Trigger Event



```
POST https://connect.mindcloud.co/v1/universal/perfit/latest/actions/send-custom-trigger-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perfit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/send-custom-trigger-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trigger_key": "string",
  "contact": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perfit/latest/actions/send-custom-trigger-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trigger_key": "string",
    "contact": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trigger_key` | string | yes | Custom trigger event key. |
| `contact` | string | yes | Contact email address. |
| `context` | object | no | Optional JSON object for template context. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Perfit API returns.

## Native endpoint

Through the native Perfit API, this operation is `POST https://webhooks.myperfit.net/events/customtriggers/app4/init/764ac753/a033319a` (base URL `https://api.myperfit.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-custom-trigger-event.md) for the provider-specific parameters and requirements.


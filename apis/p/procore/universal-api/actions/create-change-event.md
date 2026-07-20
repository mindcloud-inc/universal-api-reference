# Procore: Create Change Event

Creates a new change event in Procore.

```
POST https://connect.mindcloud.co/v1/universal/procore/latest/actions/create-change-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Procore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/procore/latest/actions/create-change-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "changeEvent": {},
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/procore/latest/actions/create-change-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "changeEvent": {},
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `changeEvent` | object | yes | Change event payload object. |
| `projectId` | string | yes | Unique identifier for the project. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Procore API returns.

## Native endpoint

Through the native Procore API, this operation is `POST /rest/v1.1/change_events` (base URL `https://api.procore.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-change-event.md) for the provider-specific parameters and requirements.


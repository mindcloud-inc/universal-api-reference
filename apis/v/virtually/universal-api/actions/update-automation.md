# Virtually: Update Automation

Updates an existing automation in Virtually.

```
PUT https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "triggerId": "string",
  "actions[]": [
    {}
  ],
  "actions[].actionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-automation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "triggerId": "string",
    "actions[]": [{}],
    "actions[].actionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |
| `triggerId` | string | yes |  |
| `actions[]` | array<object> | yes |  |
| `actions[].actionId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtually API returns.

## Native endpoint

Through the native Virtually API, this operation is `PATCH /api/v2/orgs/:orgId/automations/:id` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-automation.md) for the provider-specific parameters and requirements.


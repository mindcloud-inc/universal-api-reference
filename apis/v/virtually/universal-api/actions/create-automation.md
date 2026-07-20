# Virtually: Create Automation

Creates a new automation in Virtually.

```
POST https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "triggerId": "string",
  "actions[]": [
    {}
  ],
  "actions[].actionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-automation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `name` | string | no |  |
| `description` | string | no |  |
| `triggerId` | string | yes |  |
| `actions[]` | array<object> | yes |  |
| `actions[].actionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "triggerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `triggerId` | string |  |

## Native endpoint

Through the native Virtually API, this operation is `POST /api/v2/orgs/:orgId/automations` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-automation.md) for the provider-specific parameters and requirements.


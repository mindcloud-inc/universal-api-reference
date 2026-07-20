# Chatvolt AI: Create CRM Scenario

Creates a new CRM scenario in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-create-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-create-scenario" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-create-scenario', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name for the new CRM scenario. |
| `description` | string | no | An optional description for the CRM scenario. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Timestamp of when the scenario was created. |
| `description` | string | A description for the CRM scenario. |
| `id` | string | The unique identifier for the CRM scenario. |
| `name` | string | The name of the CRM scenario. |
| `organizationId` | string | The ID of the organization this scenario belongs to. |
| `updatedAt` | string | Timestamp of when the scenario was last updated. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /crm/scenario` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-scenario-create-scenario.md) for the provider-specific parameters and requirements.


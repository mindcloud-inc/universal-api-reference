# Chatvolt AI: Update CRM Scenario

Updates an existing CRM scenario in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-update-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-update-scenario" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-update-scenario', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the CRM scenario to update. |
| `name` | string | yes | The new name for the CRM scenario. |
| `description` | string | no | An optional new description for the CRM scenario. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "scenario": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Message. |
| `scenario` | object | Scenario. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PUT /crm/scenario` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-scenario-update-scenario.md) for the provider-specific parameters and requirements.


# Pingueen: Assign Client Agents



```
PUT https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/assign-client-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingueen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/assign-client-agents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agents[]": [
    {}
  ],
  "agents[].agent": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/assign-client-agents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agents[]": [{}],
    "agents[].agent": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agents[]` | array<object> | yes | Agent assignments to apply. |
| `agents[].agent` | string | yes | Agent identifier to assign. |
| `agents[].dtUntil` | date | no | ISO 8601 expiration date for the assignment. |
| `id` | string | yes | Customer ID to assign agents to. |
| `notes` | string | no | Optional notes for the assignment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Assignment result details returned by Pingueen. |
| `success` | boolean | Whether the agents were assigned successfully. |

## Native endpoint

Through the native Pingueen API, this operation is `POST /clients/:_id/assign-agents` (base URL `https://api.pingueen.it/ext/v2/{{credentials.businessname}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-client-agents.md) for the provider-specific parameters and requirements.


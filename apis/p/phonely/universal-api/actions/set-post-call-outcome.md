# Phonely: Set Post-Call Outcome

Updates a post-call outcome in Phonely.

```
PUT https://connect.mindcloud.co/v1/universal/phonely/latest/actions/set-post-call-outcome
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/set-post-call-outcome" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "callIdOrPhone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phonely/latest/actions/set-post-call-outcome', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "callIdOrPhone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `callIdOrPhone` | string | yes |  |
| `customCallOutcome` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customCallOutcomeValue` | number | no |  |
| `customCallMetadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": "string",
      "call_id": "string",
      "success": true,
      "updated_fields": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | string |  |
| `call_id` | string |  |
| `success` | boolean |  |
| `updated_fields` | array<string> |  |

## Native endpoint

Through the native Phonely API, this operation is `PATCH /api/calls/{{agentId}}/{{callIdOrPhone}}` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-post-call-outcome.md) for the provider-specific parameters and requirements.


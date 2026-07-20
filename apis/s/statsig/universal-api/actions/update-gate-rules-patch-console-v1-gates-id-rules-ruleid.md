# Statsig: Update Gate Rules

Updates gate rules in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-gate-rules-patch-console-v1-gates-id-rules-ruleid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-gate-rules-patch-console-v1-gates-id-rules-ruleid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "ruleID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-gate-rules-patch-console-v1-gates-id-rules-ruleid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "ruleID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Gate ID |
| `ruleID` | string | yes | Rule ID |
| `name` | string | no | Request body field. |
| `passPercentage` | number | no | Request body field. |
| `conditions` | list | no | Request body field. |
| `environments` | list | no | Request body field. |
| `baseID` | string | no | Request body field. |
| `returnValue` | object | no | Request body field. |
| `completedAutomatedRollouts` | list | no | Request body field. |
| `pendingAutomatedRollouts` | list | no | Request body field. |
| `conditions` | object | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PATCH /console/v1/gates/{id}/rules/{ruleID}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-gate-rules-patch-console-v1-gates-id-rules-ruleid.md) for the provider-specific parameters and requirements.


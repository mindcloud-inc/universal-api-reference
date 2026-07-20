# Zapier NLA: Execute Exposed Action



```
POST https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/execute-exposed-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zapier NLA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/execute-exposed-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "exposed_app_action_id": "string",
  "instructions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/execute-exposed-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "exposed_app_action_id": "string",
    "instructions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `exposed_app_action_id` | string | yes | The UUID of the exposed Zapier action to execute. |
| `instructions` | string | yes | Plain-English instructions for the exposed action. This is required by Zapier. |
| `previewOnly` | boolean | no | When true, Zapier previews the action without executing it. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_used": "string",
      "additional_results": [
        {}
      ],
      "assistant_hint": "string",
      "error": "string",
      "id": "string",
      "input_params": {},
      "result": {},
      "result_field_labels": {},
      "review_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_used` | string |  |
| `additional_results` | array<object> |  |
| `assistant_hint` | string |  |
| `error` | string |  |
| `id` | string |  |
| `input_params` | object |  |
| `result` | object |  |
| `result_field_labels` | object |  |
| `review_url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zapier NLA API, this operation is `POST /api/v1/exposed/:exposed_app_action_id/execute/` (base URL `https://actions.zapier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-exposed-action.md) for the provider-specific parameters and requirements.


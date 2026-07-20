# Zapier NLA: Get Execution Log



```
GET https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/get-execution-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zapier NLA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/get-execution-log?connectionId=$CONNECTION_ID&execution_log_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "execution_log_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/get-execution-log?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `execution_log_id` | string | yes | Execution log UUID to retrieve. |

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

Through the native Zapier NLA API, this operation is `GET /api/v1/execution-log/:execution_log_id/` (base URL `https://actions.zapier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-execution-log.md) for the provider-specific parameters and requirements.


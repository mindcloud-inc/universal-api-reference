# Lakera AI Guardrails: Check Policy Health



```
GET https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/check-policy-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lakera AI Guardrails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/check-policy-health?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/check-policy-health?${params}`, {
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
| `projectId` | string | yes | Lakera project ID whose policy configuration health should be checked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isDefault": true,
      "lint": {
        "errors": [
          {}
        ],
        "passed": true
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDefault` | boolean | Whether the result is for the default policy. |
| `lint` | object | Nested policy validation results. |
| `lint.errors` | array<object> | Nested policy validation errors and warnings. |
| `lint.passed` | boolean | Whether nested policy validation passed. |
| `message` | string | Human-readable policy health message. |
| `status` | string | Overall policy health status. |

## Native endpoint

Through the native Lakera AI Guardrails API, this operation is `POST /policies/health` (base URL `https://api.lakera.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-policy-health.md) for the provider-specific parameters and requirements.


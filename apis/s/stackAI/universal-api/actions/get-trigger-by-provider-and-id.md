# Stack AI: Get Trigger by Provider and ID



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-trigger-by-provider-and-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-trigger-by-provider-and-id?connectionId=$CONNECTION_ID&providerId=string&triggerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "providerId": "string",
  "triggerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-trigger-by-provider-and-id?${params}`, {
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
| `providerId` | string | yes | The provider identifier. |
| `triggerId` | string | yes | The trigger identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can_get_test_samples": true,
      "description": "string",
      "input_param_count": 1,
      "name": "Ava Chen",
      "output_param_count": 1,
      "provider_id": "string",
      "supports_test_ui": true,
      "tags": [
        "string"
      ],
      "trigger_id": "string",
      "trigger_type": "string",
      "webhook_requires_verification": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_get_test_samples` | boolean | Whether test samples are available. |
| `description` | string | The trigger description. |
| `input_param_count` | number | How many input parameters the trigger exposes. |
| `name` | string | The trigger name. |
| `output_param_count` | number | How many output parameters the trigger exposes. |
| `provider_id` | string | The provider identifier. |
| `supports_test_ui` | boolean | Whether test UI is supported. |
| `tags` | array<string> | Trigger tags. |
| `trigger_id` | string | The trigger identifier. |
| `trigger_type` | string | The trigger type. |
| `webhook_requires_verification` | boolean | Whether webhook verification is required. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /tools/stackai/providers/:provider_id/triggers/:trigger_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trigger-by-provider-and-id.md) for the provider-specific parameters and requirements.


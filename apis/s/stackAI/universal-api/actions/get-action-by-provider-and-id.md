# Stack AI: Get Action by Provider and ID



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-by-provider-and-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-by-provider-and-id?connectionId=$CONNECTION_ID&actionId=string&providerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "string",
  "providerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-by-provider-and-id?${params}`, {
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
| `actionId` | string | yes | The action identifier. |
| `providerId` | string | yes | The provider identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_id": "string",
      "deprecated": true,
      "input_param_count": 1,
      "is_searchable": true,
      "name": "Ava Chen",
      "output_param_count": 1,
      "provider_id": "string",
      "tags": [
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
| `action_id` | string | The action identifier. |
| `deprecated` | boolean | Whether the action is deprecated. |
| `input_param_count` | number | How many input parameters the action expects. |
| `is_searchable` | boolean | Whether the action is searchable. |
| `name` | string | The action name. |
| `output_param_count` | number | How many output parameters the action returns. |
| `provider_id` | string | The provider identifier. |
| `tags` | array<string> | Action tags. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /tools/stackai/providers/:provider_id/actions/:action_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-by-provider-and-id.md) for the provider-specific parameters and requirements.


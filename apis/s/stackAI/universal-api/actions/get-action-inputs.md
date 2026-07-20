# Stack AI: Get Action Inputs



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-inputs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-inputs?connectionId=$CONNECTION_ID&actionId=string&providerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "string",
  "providerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-inputs?${params}`, {
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
      "required": [
        "string"
      ],
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `required` | array<string> | Required property names. |
| `title` | string | The schema title. |
| `type` | string | The schema root type. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /tools/stackai/providers/:provider_id/actions/:action_id/inputs` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-inputs.md) for the provider-specific parameters and requirements.


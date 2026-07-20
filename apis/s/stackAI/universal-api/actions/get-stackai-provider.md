# Stack AI: Get StackAI Provider



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-stackai-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-stackai-provider?connectionId=$CONNECTION_ID&providerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "providerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-stackai-provider?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_count": 1,
      "color": "string",
      "description": "string",
      "icon": "string",
      "labels": [
        "string"
      ],
      "name": "Ava Chen",
      "provider_group": [
        "string"
      ],
      "provider_id": "string",
      "provider_version": "string",
      "tags": [
        "string"
      ],
      "trigger_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_count` | number | How many actions the provider exposes. |
| `color` | string | The provider accent color. |
| `description` | string | The provider description. |
| `icon` | string | The provider icon URL. |
| `labels` | array<string> | Provider labels. |
| `name` | string | The provider name. |
| `provider_group` | array<string> | Provider group classifications. |
| `provider_id` | string | The provider identifier. |
| `provider_version` | string | The provider version. |
| `tags` | array<string> | Provider tags. |
| `trigger_count` | number | How many triggers the provider exposes. |

## Native endpoint

Through the native Stack AI API, this operation is `GET /tools/stackai/providers/:provider_id` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stackai-provider.md) for the provider-specific parameters and requirements.


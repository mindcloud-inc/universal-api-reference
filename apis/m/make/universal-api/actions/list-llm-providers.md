# Make: List LLM Providers

Lists LLM providers for the specified team.

```
GET https://connect.mindcloud.co/v1/universal/make/latest/actions/list-llm-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Make `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/list-llm-providers?connectionId=$CONNECTION_ID&teamId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/make/latest/actions/list-llm-providers?${params}`, {
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
| `teamId` | number | yes | The ID of the Make team whose LLM providers should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "id": 1,
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `id` | number |  |
| `provider` | string |  |

## Native endpoint

Through the native Make API, this operation is `GET /ai-agents/v1/llm-providers` (base URL `https://us2.make.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-llm-providers.md) for the provider-specific parameters and requirements.


# Port API AI: Get AI Invocation

Retrieves an AI invocation from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-ai-invocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-ai-invocation?connectionId=$CONNECTION_ID&invocationIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invocationIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-ai-invocation?${params}`, {
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
| `invocationIdentifier` | string | yes | The AI invocation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /ai/invoke/:invocation_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-invocation.md) for the provider-specific parameters and requirements.


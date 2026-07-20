# Handelsregister AI: List API Tokens

Retrieves a list of API tokens from Handelsregister AI.

```
GET https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/list-api-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handelsregister AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/list-api-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/list-api-tokens?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "tokens": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Provider metadata, including credit information. |
| `tokens` | array<object> | Available API tokens. |
| `total` | number | Total number of tokens. |

## Native endpoint

Through the native Handelsregister AI API, this operation is `GET /auth/tokens` (base URL `https://handelsregister.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-tokens.md) for the provider-specific parameters and requirements.


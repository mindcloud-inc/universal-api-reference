# Documently: List API Tokens

Retrieves API tokens from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-api-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-api-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-api-tokens?${params}`, {
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
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "hydra:member": [
        {}
      ],
      "hydra:totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `hydra:member` | array<object> |  |
| `hydra:totalItems` | number |  |

## Native endpoint

Through the native Documently API, this operation is `GET /api-tokens` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-tokens.md) for the provider-specific parameters and requirements.


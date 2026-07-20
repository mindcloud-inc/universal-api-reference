# Cohere: Detokenize

Converts Cohere token IDs back into text.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/detokenize
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/detokenize?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/detokenize?${params}`, {
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
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `text` | string |  |

## Native endpoint

Through the native Cohere API, this operation is `POST /v1/detokenize` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detokenize.md) for the provider-specific parameters and requirements.


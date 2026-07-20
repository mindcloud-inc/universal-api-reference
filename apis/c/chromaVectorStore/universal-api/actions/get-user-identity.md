# Chroma Vector Store: Get User Identity

Retrieves user identity details from Chroma.

```
GET https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/get-user-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/get-user-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/get-user-identity?${params}`, {
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
      "databases": [
        "string"
      ],
      "tenant": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databases` | array<string> |  |
| `tenant` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Chroma Vector Store API, this operation is `GET /api/v2/auth/identity` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-identity.md) for the provider-specific parameters and requirements.


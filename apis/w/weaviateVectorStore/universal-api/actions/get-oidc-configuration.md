# Weaviate Vector Store: Get OIDC Configuration

Retrieves OIDC configuration from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-oidc-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-oidc-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-oidc-configuration?${params}`, {
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
      "authorization_endpoint": "string",
      "id_token_signing_alg_values_supported": [
        [
          "string"
        ]
      ],
      "issuer": "string",
      "jwks_uri": "string",
      "response_types_supported": [
        [
          "string"
        ]
      ],
      "subject_types_supported": [
        [
          "string"
        ]
      ],
      "token_endpoint": "string",
      "userinfo_endpoint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorization_endpoint` | string |  |
| `id_token_signing_alg_values_supported[]` | array<string> |  |
| `issuer` | string |  |
| `jwks_uri` | string |  |
| `response_types_supported[]` | array<string> |  |
| `subject_types_supported[]` | array<string> |  |
| `token_endpoint` | string |  |
| `userinfo_endpoint` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /.well-known/openid-configuration` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oidc-configuration.md) for the provider-specific parameters and requirements.


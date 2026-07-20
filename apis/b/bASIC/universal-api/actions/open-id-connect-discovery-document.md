# BASIC: OpenID Connect Discovery Document

Retrieves the OpenID Connect discovery document from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/open-id-connect-discovery-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/open-id-connect-discovery-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/open-id-connect-discovery-document?${params}`, {
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
      "grant_types_supported": [
        [
          "string"
        ]
      ],
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
      "scopes_supported": [
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
      "token_endpoint_auth_methods_supported": [
        [
          "string"
        ]
      ],
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
| `grant_types_supported[]` | array<string> |  |
| `id_token_signing_alg_values_supported[]` | array<string> |  |
| `issuer` | string |  |
| `jwks_uri` | string |  |
| `response_types_supported[]` | array<string> |  |
| `scopes_supported[]` | array<string> |  |
| `subject_types_supported[]` | array<string> |  |
| `token_endpoint` | string |  |
| `token_endpoint_auth_methods_supported[]` | array<string> |  |
| `userinfo_endpoint` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /auth/.well-known/openid-configuration` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-id-connect-discovery-document.md) for the provider-specific parameters and requirements.


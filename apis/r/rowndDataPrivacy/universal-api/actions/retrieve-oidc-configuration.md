# Rownd Data Privacy: Retrieve OIDC Configuration



```
GET https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/retrieve-oidc-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/retrieve-oidc-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/retrieve-oidc-configuration?${params}`, {
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
      "claims_supported": [
        "string"
      ],
      "code_challenge_methods_supported": [
        "string"
      ],
      "grant_types_supported": [
        "string"
      ],
      "id_token_signing_alg_values_supported": [
        "string"
      ],
      "introspection_endpoint_auth_methods_supported": [
        "string"
      ],
      "issuer": "string",
      "jwks_uri": "string",
      "request_object_signing_alg_values_supported": [
        "string"
      ],
      "request_parameter_supported": true,
      "response_types_supported": [
        "string"
      ],
      "revocation_endpoint_auth_methods_supported": [
        "string"
      ],
      "scopes_supported": [
        "string"
      ],
      "subject_types_supported": [
        "string"
      ],
      "token_endpoint": "string",
      "token_endpoint_auth_methods_supported": [
        "string"
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
| `claims_supported` | array<string> |  |
| `code_challenge_methods_supported` | array<string> |  |
| `grant_types_supported` | array<string> |  |
| `id_token_signing_alg_values_supported` | array<string> |  |
| `introspection_endpoint_auth_methods_supported` | array<string> |  |
| `issuer` | string |  |
| `jwks_uri` | string |  |
| `request_object_signing_alg_values_supported` | array<string> |  |
| `request_parameter_supported` | boolean |  |
| `response_types_supported` | array<string> |  |
| `revocation_endpoint_auth_methods_supported` | array<string> |  |
| `scopes_supported` | array<string> |  |
| `subject_types_supported` | array<string> |  |
| `token_endpoint` | string |  |
| `token_endpoint_auth_methods_supported` | array<string> |  |
| `userinfo_endpoint` | string |  |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `GET https://api.rownd.io/hub/auth/.well-known/oauth-authorization-server` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-oidc-configuration.md) for the provider-specific parameters and requirements.


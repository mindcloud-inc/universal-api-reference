# Neon: Update OAuth provider

Updates an OAuth provider in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-oauth-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-oauth-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "oauth_provider_id": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-oauth-provider', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "oauth_provider_id": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `oauth_provider_id` | list | yes | Neon API parameter oauth_provider_id One of: `0`, `1`, `2`, `3`. |
| `client_id` | string | no | Neon API parameter client_id |
| `client_secret` | string | no | Neon API parameter client_secret |
| `microsoft_tenant_id` | string | no | Neon API parameter microsoft_tenant_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": "string",
      "client_secret": "string",
      "id": [
        "string"
      ],
      "type": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string |  |
| `client_secret` | string |  |
| `id` | array |  |
| `type` | array |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /projects/:project_id/auth/oauth_providers/:oauth_provider_id` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-neon-auth-oauth-provider.md) for the provider-specific parameters and requirements.


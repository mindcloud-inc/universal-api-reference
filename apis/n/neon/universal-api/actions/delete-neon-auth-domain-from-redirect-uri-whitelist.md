# Neon: Delete domain from redirect_uri whitelist

Deletes trusted redirect URI domain from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-neon-auth-domain-from-redirect-uri-whitelist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-neon-auth-domain-from-redirect-uri-whitelist?connectionId=$CONNECTION_ID&project_id=string&auth_provider=0&domains%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "auth_provider": "0",
  "domains[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-neon-auth-domain-from-redirect-uri-whitelist?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |
| `auth_provider` | list | yes | Neon API parameter auth_provider One of: `0`, `1`, `2`, `3`. |
| `domains[]` | array<object> | yes | Neon API parameter domains |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /projects/:project_id/auth/domains` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-neon-auth-domain-from-redirect-uri-whitelist.md) for the provider-specific parameters and requirements.


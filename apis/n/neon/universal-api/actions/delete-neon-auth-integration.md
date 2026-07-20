# Neon: Delete integration with auth provider

Deletes an auth provider integration from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-neon-auth-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-neon-auth-integration?connectionId=$CONNECTION_ID&project_id=string&auth_provider=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "auth_provider": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-neon-auth-integration?${params}`, {
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
| `delete_data` | boolean | no | Neon API parameter delete_data |

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

Through the native Neon API, this operation is `DELETE /projects/:project_id/auth/integration/:auth_provider` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-neon-auth-integration.md) for the provider-specific parameters and requirements.


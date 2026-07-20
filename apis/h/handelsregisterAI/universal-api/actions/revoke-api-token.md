# Handelsregister AI: Revoke API Token

Revokes an existing API token from Handelsregister AI.

```
DELETE https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/revoke-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handelsregister AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/revoke-api-token?connectionId=$CONNECTION_ID&id=16" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "16"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/revoke-api-token?${params}`, {
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
| `id` | number | yes | ID of the API token to revoke. Example: `16`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "meta": {},
      "token_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message. |
| `meta` | object | Provider metadata for the revoke request. |
| `token_name` | string | Name of the revoked token. |

## Native endpoint

Through the native Handelsregister AI API, this operation is `DELETE /auth/tokens/:id` (base URL `https://handelsregister.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-api-token.md) for the provider-specific parameters and requirements.


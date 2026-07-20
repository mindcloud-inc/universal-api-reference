# Perplexity: Revoke Auth Token

Revokes an auth token in Perplexity.

```
DELETE https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/revoke-auth-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/revoke-auth-token?connectionId=$CONNECTION_ID&authToken=pplx-1234567890abcdef" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "pplx-1234567890abcdef"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/revoke-auth-token?${params}`, {
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
| `authToken` | string | yes | Example: `pplx-1234567890abcdef`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Perplexity API returns.

## Native endpoint

Through the native Perplexity API, this operation is `POST /revoke_auth_token` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-auth-token.md) for the provider-specific parameters and requirements.


# Walmart: Token API - authorization_code



```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/token-api-authorization-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/token-api-authorization-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/token-api-authorization-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `grant_type` | list<string> | no | Default: `authorization_code`. |
| `redirectUri` | string | no | Default: `https://api.mindcloud.co/v1/oauth/walmart/callback`. |
| `code` | string | no | Default: `65CA5DA313A549D49D15D3119D9AD85D`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Walmart API returns.

## Native endpoint

Through the native Walmart API, this operation is `POST v3/token` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/token-api-authorization-code.md) for the provider-specific parameters and requirements.


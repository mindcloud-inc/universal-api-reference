# Scrapeless: Configure 1Password Integration

Updates the 1Password integration in Scrapeless.

```
PUT https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/configure-1password-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/configure-1password-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/configure-1password-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xApiToken` | string | no | API key for authentication |
| `name` | string | yes | Integration name used to identify this 1Password integration configuration |
| `token` | string | yes | 1Password API access token for securely accessing your 1Password vault. This should be a service account token starting with 'ops_' |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrapeless API returns.

## Native endpoint

Through the native Scrapeless API, this operation is `PUT /browser/one-password/token` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-1password-integration.md) for the provider-specific parameters and requirements.


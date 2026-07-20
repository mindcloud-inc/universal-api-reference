# Explodely: Create Affiliate User

Creates a new affiliate user in Explodely.

```
POST https://connect.mindcloud.co/v1/universal/explodely/latest/actions/create-affiliate-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/create-affiliate-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affiliateUsername": "codex_affiliate_001",
  "userPassword": "SandboxPass123!",
  "firstName": "Codex",
  "lastName": "Sandbox",
  "email": "sandbox-affiliate@example.com",
  "ipAddress": "127.0.0.1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explodely/latest/actions/create-affiliate-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affiliateUsername": "codex_affiliate_001",
    "userPassword": "SandboxPass123!",
    "firstName": "Codex",
    "lastName": "Sandbox",
    "email": "sandbox-affiliate@example.com",
    "ipAddress": "127.0.0.1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliateUsername` | string | yes | The username for the affiliate account you want to create. Example: `codex_affiliate_001`. |
| `userPassword` | string | yes | The password for the new affiliate account. Example: `SandboxPass123!`. |
| `firstName` | string | yes | The affiliate user's first name. Example: `Codex`. |
| `lastName` | string | yes | The affiliate user's last name. Example: `Sandbox`. |
| `email` | string | yes | The affiliate user's email address. Example: `sandbox-affiliate@example.com`. |
| `ipAddress` | string | yes | The affiliate user's IP address. Example: `127.0.0.1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "usercreated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `usercreated` | string |  |

## Native endpoint

Through the native Explodely API, this operation is `POST /aff` (base URL `https://explodely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-affiliate-user.md) for the provider-specific parameters and requirements.


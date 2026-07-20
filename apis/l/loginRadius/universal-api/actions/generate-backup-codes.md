# LoginRadius: Generate Backup Codes

Retrieves MFA backup codes from LoginRadius.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/generate-backup-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/generate-backup-codes?connectionId=$CONNECTION_ID&accessToken=seeded-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "seeded-access-token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/generate-backup-codes?${params}`, {
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
| `accessToken` | string | yes | Access Token of the user. Example: `seeded-access-token`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/auth/account/2fa/backupcode` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-backup-codes.md) for the provider-specific parameters and requirements.


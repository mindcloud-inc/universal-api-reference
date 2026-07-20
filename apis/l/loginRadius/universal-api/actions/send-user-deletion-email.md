# LoginRadius: Send User Deletion Email

Sends a user deletion email from LoginRadius.

```
DELETE https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/send-user-deletion-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/send-user-deletion-email?connectionId=$CONNECTION_ID&accessToken=seeded-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "seeded-access-token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/send-user-deletion-email?${params}`, {
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
| `accessToken` | string | yes | Access Token of the user requesting account deletion email. Example: `seeded-access-token`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailTemplate` | string | no | Optional LoginRadius email template name for the deletion message. Example: `delete-account-request`. |
| `deleteUrl` | string | no | Optional delete confirmation URL included in the deletion email. Example: `https://example.com/delete-account`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isDeleteRequestAccepted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDeleteRequestAccepted` | boolean | Whether LoginRadius accepted the user-deletion email request. |

## Native endpoint

Through the native LoginRadius API, this operation is `DELETE /identity/v2/auth/account` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-user-deletion-email.md) for the provider-specific parameters and requirements.


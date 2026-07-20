# LoginRadius: Delete Account by Email

Deletes an existing account from LoginRadius by email.

```
DELETE https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-account-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-account-by-email?connectionId=$CONNECTION_ID&email=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-account-by-email?${params}`, {
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
| `email` | string | yes | Email address of the account to delete. Example: `user@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preventWebhook` | boolean | no | Whether to suppress LoginRadius webhook processing for the delete operation. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isDeleted": true,
      "recordsDeleted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDeleted` | boolean | Whether LoginRadius deleted the matching account. |
| `recordsDeleted` | number | Number of records deleted by the operation. |

## Native endpoint

Through the native LoginRadius API, this operation is `DELETE /identity/v2/manage/account` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-account-by-email.md) for the provider-specific parameters and requirements.


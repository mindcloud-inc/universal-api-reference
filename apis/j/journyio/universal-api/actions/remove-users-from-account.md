# Journy.io: Remove Users from Account



```
DELETE https://connect.mindcloud.co/v1/universal/journyio/latest/actions/remove-users-from-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Journy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/remove-users-from-account?connectionId=$CONNECTION_ID&users%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "users[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/journyio/latest/actions/remove-users-from-account?${params}`, {
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
| `account.accountId` | string | no | Unique identifier for the account in your database. |
| `account.domain` | string | no | The domain associated with the account. |
| `users[]` | array<object> | yes | Users to remove from the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "meta": {
        "requestId": "string",
        "status": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `meta.requestId` | string |  |
| `meta.status` | number |  |

## Native endpoint

Through the native Journy.io API, this operation is `POST /accounts/users/remove` (base URL `https://api.journy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-users-from-account.md) for the provider-specific parameters and requirements.


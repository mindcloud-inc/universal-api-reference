# LoginRadius: Delete Account by UID

Deletes an existing account from LoginRadius by UID.

```
DELETE https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-account-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-account-by-uid?connectionId=$CONNECTION_ID&uid=loginradius-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "loginradius-uid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/delete-account-by-uid?${params}`, {
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
| `uid` | string | yes | UID of the account to delete. Example: `loginradius-uid`. |

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
      "isDeleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDeleted` | boolean | Whether LoginRadius deleted the target account. |

## Native endpoint

Through the native LoginRadius API, this operation is `DELETE /identity/v2/manage/account/:uid` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-account-by-uid.md) for the provider-specific parameters and requirements.


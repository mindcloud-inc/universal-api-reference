# ActivityInfo: List Billing Account Users

Retrieves users for an ActivityInfo billing account.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-users?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-users?${params}`, {
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
| `accountId` | string | yes | ActivityInfo billing account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAccountRole": "string",
      "email": "ava@example.com",
      "lastLoginTime": 1,
      "name": "Ava Chen",
      "userId": "string",
      "userLicenseType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAccountRole` | string | Billing account role. |
| `email` | string | User email. |
| `lastLoginTime` | number | Last login time in milliseconds since epoch. |
| `name` | string | User name. |
| `userId` | string | User ID. |
| `userLicenseType` | string | Required license type. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/billingAccounts/:accountId/users` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-account-users.md) for the provider-specific parameters and requirements.


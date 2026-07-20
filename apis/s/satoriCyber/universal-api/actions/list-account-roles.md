# Satori Cyber: List Account Roles

Retrieves roles for an account in Satori Cyber.

```
GET https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/list-account-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satori Cyber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/list-account-roles?connectionId=$CONNECTION_ID&accountId=acc_12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "acc_12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/list-account-roles?${params}`, {
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
| `accountId` | string | yes | Satori account ID. Example: `acc_12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "hasMultipleRoleSupport": true,
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `hasMultipleRoleSupport` | boolean |  |
| `records` | array<object> |  |

## Native endpoint

Through the native Satori Cyber API, this operation is `GET /api/accounts/:accountId/roles` (base URL `https://app.satoricyber.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-roles.md) for the provider-specific parameters and requirements.


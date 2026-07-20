# Connecteam: List User Balances

Retrieve a list of user time-off balances within a policy type

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-user-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-user-balances?connectionId=$CONNECTION_ID&limit=25&offset=0&policyTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "policyTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-user-balances?${params}`, {
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
| `policyTypeId` | string | yes |  |
| `userIds` | array<number> | no | Accepts multiple values as an array. |
| `limit` | number | no | Default: `10`. |
| `offset` | number | no | Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "units": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `units` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /time-off/v1/policy-types/:policyTypeId/balances` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-balances.md) for the provider-specific parameters and requirements.


# ProfitWell: Get Subscription History For User

Retrieves subscription history for a user from ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-subscription-history-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-subscription-history-for-user?connectionId=$CONNECTION_ID&userIdOrUserAlias=spiderman" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIdOrUserAlias": "spiderman"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-subscription-history-for-user?${params}`, {
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
| `userIdOrUserAlias` | string | yes | Either the user_id or the user_alias of the user. Example: `spiderman`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "effective_date": 1,
      "email": "ava@example.com",
      "meta": {},
      "plan_currency": "string",
      "plan_id": "string",
      "plan_interval": "string",
      "status": "string",
      "subscription_alias": "string",
      "subscription_id": "string",
      "user_alias": "string",
      "user_id": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effective_date` | number |  |
| `email` | string |  |
| `meta` | object |  |
| `plan_currency` | string |  |
| `plan_id` | string |  |
| `plan_interval` | string |  |
| `status` | string |  |
| `subscription_alias` | string |  |
| `subscription_id` | string |  |
| `user_alias` | string |  |
| `user_id` | string |  |
| `value` | number |  |

## Native endpoint

Through the native ProfitWell API, this operation is `GET /v2/users/:userIdOrUserAlias/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-history-for-user.md) for the provider-specific parameters and requirements.


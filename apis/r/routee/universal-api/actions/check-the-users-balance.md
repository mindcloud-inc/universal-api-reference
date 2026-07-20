# Routee: Check the user’s balance

Retrieves the current user balance from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-the-users-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-the-users-balance?connectionId=$CONNECTION_ID&uSD=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uSD": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-the-users-balance?${params}`, {
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
| `uSD` | string | yes | Optional parameter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance_currency": 1,
      "currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance_currency` | number |  |
| `currency` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /balance` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-the-users-balance.md) for the provider-specific parameters and requirements.


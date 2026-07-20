# Recurly: Fetch Account Balance



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-account-balance?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-account-balance?${params}`, {
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
| `accountId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "balances": [
        {}
      ],
      "object": "string",
      "pastDue": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `balances` | array<object> |  |
| `object` | string |  |
| `pastDue` | boolean |  |

## Native endpoint

Through the native Recurly API, this operation is `GET /accounts/:account_id/balance` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-account-balance.md) for the provider-specific parameters and requirements.


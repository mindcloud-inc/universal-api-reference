# Brevo: Get Loyalty Subscription Balances



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-loyalty-subscription-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-loyalty-subscription-balances?connectionId=$CONNECTION_ID&cid=string&pid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cid": "string",
  "pid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-loyalty-subscription-balances?${params}`, {
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
| `cid` | string | yes |  |
| `pid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items` | array<object> |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/loyalty/balance/programs/:pid/subscriptions/:cid/balances` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-loyalty-subscription-balances.md) for the provider-specific parameters and requirements.


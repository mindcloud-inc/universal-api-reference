# Didit: Top Up Credits

Creates a credit top-up request in Didit.

```
POST https://connect.mindcloud.co/v1/universal/didit/latest/actions/top-up-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/didit/latest/actions/top-up-credits" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amountInDollars": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/didit/latest/actions/top-up-credits', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amountInDollars": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amountInDollars` | number | yes |  |
| `cancelUrl` | string | no |  |
| `successUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutSessionId": "string",
      "checkoutSessionUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutSessionId` | string |  |
| `checkoutSessionUrl` | string |  |

## Native endpoint

Through the native Didit API, this operation is `POST /billing/top-up/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/top-up-credits.md) for the provider-specific parameters and requirements.


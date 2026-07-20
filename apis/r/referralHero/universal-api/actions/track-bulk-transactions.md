# ReferralHero: Track Bulk Transactions

Creates bulk subscriber transactions in ReferralHero.

```
POST https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/track-bulk-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/track-bulk-transactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactions[]": [
    {}
  ],
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/track-bulk-transactions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactions[]": [{}],
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactions[]` | array<object> | yes | JSON array of transactions to process in bulk. |
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ReferralHero API, this operation is `POST /lists/:uuid/subscribers/add_bulk_transactions` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-bulk-transactions.md) for the provider-specific parameters and requirements.


# Referral Rock: List Payout Transactions

Retrieves payout transactions from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-payout-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-payout-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-payout-transactions?${params}`, {
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
| `recipientId` | string | no | The unique ID of the recipient of the payout transaction. |
| `transactionId` | string | no | The unique ID of the payout transaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createDate": "2026-05-07T12:00:00.000Z",
      "externalIdentifier": "string",
      "id": "string",
      "recipientId": "string",
      "status": "string",
      "transactionDestination": "string",
      "transactionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createDate` | date |  |
| `externalIdentifier` | string |  |
| `id` | string |  |
| `recipientId` | string |  |
| `status` | string |  |
| `transactionDestination` | string |  |
| `transactionType` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/payouts/transactions` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payout-transactions.md) for the provider-specific parameters and requirements.


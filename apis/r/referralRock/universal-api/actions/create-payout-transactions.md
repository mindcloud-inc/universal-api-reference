# Referral Rock: Create Payout Transactions

Creates payout transactions for pending Referral Rock rewards.

```
POST https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-payout-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-payout-transactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payoutId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-payout-transactions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payoutId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `overrideIneligible` | boolean | no | Allows payouts for rewards with eligibility dates in the future. |
| `memberId` | string | no | Deprecated member identifier for the payout recipient. |
| `recipientId` | string | no | The unique ID of the recipient to whom payouts will be issued. |
| `payoutId` | string | yes | The payout type whose pending amounts should be issued. |
| `note` | string | no | Message to send to the recipient of the issued payout. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issuePayoutTransactionResults": [
        {
          "payoutTransaction": {
            "amount": 1,
            "createDate": "string",
            "currencyCode": "string",
            "externalIdentifier": "string",
            "id": "string",
            "recipientId": "string",
            "status": "string",
            "transactionDestination": "string",
            "transactionType": "string",
            "vendorErrorMessage": {},
            "vendorErrorStatus": {}
          },
          "resultInfo": {
            "message": "string",
            "status": "string"
          }
        }
      ],
      "message": {},
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issuePayoutTransactionResults[].payoutTransaction.amount` | number |  |
| `issuePayoutTransactionResults[].payoutTransaction.createDate` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.currencyCode` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.externalIdentifier` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.id` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.recipientId` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.status` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.transactionDestination` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.transactionType` | string |  |
| `issuePayoutTransactionResults[].payoutTransaction.vendorErrorMessage` | object |  |
| `issuePayoutTransactionResults[].payoutTransaction.vendorErrorStatus` | object |  |
| `issuePayoutTransactionResults[].resultInfo.message` | string |  |
| `issuePayoutTransactionResults[].resultInfo.status` | string |  |
| `message` | object |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/payouts/transactions` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payout-transactions.md) for the provider-specific parameters and requirements.


# Atlar: Update transaction

Updates an existing transaction in Atlar.

```
PUT https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/update-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string<string> | yes |  |
| `If_Match` | string<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "amount": {},
      "attachedTransactables": [
        {}
      ],
      "bankTransactionCode": {},
      "batchInformation": {},
      "charges": [
        {}
      ],
      "counterparty": {},
      "currencyExchange": {},
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "instructedAmount": {},
      "organizationId": "string",
      "reconciliationStatus": "string",
      "reference": "string",
      "references": {},
      "returned": true,
      "returnReason": {},
      "valueDate": "2026-05-07T12:00:00.000Z",
      "virtualAccount": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `amount` | object |  |
| `attachedTransactables` | array<object> |  |
| `bankTransactionCode` | object |  |
| `batchInformation` | object |  |
| `charges` | array<object> |  |
| `counterparty` | object |  |
| `currencyExchange` | object |  |
| `date` | date |  |
| `description` | string |  |
| `id` | string |  |
| `instructedAmount` | object |  |
| `organizationId` | string |  |
| `reconciliationStatus` | string |  |
| `reference` | string |  |
| `references` | object |  |
| `returned` | boolean |  |
| `returnReason` | object |  |
| `valueDate` | date |  |
| `virtualAccount` | object |  |

## Native endpoint

Through the native Atlar API, this operation is `PATCH /financial-data/v2/transactions/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transaction.md) for the provider-specific parameters and requirements.


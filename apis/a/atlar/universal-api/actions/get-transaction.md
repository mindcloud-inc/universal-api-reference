# Atlar: Get transaction

Retrieves a transaction from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-transaction?${params}`, {
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
| `id` | string<string> | yes |  |

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

Through the native Atlar API, this operation is `GET /financial-data/v2/transactions/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.


# Fatture in Cloud: Create Receipt

Creates a new receipt in Fatture in Cloud.

```
POST https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | The ID of the company. |
| `data` | object | yes | The receipt payload inside the provider data envelope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountGross": 1,
      "amountNet": 1,
      "amountVat": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "itemsList": [
        {
          "amountGross": 1,
          "amountNet": 1,
          "amountVat": 1,
          "category": "string",
          "id": 1,
          "vat": {
            "description": "string",
            "id": 1,
            "value": 1
          }
        }
      ],
      "number": 1,
      "numeration": "string",
      "paymentAccount": {
        "id": 1,
        "name": "Ava Chen"
      },
      "rcCenter": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "useGrossPrices": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountGross` | number |  |
| `amountNet` | number |  |
| `amountVat` | number |  |
| `createdAt` | date |  |
| `date` | date |  |
| `description` | string |  |
| `id` | number |  |
| `itemsList[].amountGross` | number |  |
| `itemsList[].amountNet` | number |  |
| `itemsList[].amountVat` | number |  |
| `itemsList[].category` | string |  |
| `itemsList[].id` | number |  |
| `itemsList[].vat.description` | string |  |
| `itemsList[].vat.id` | number |  |
| `itemsList[].vat.value` | number |  |
| `number` | number |  |
| `numeration` | string |  |
| `paymentAccount.id` | number |  |
| `paymentAccount.name` | string |  |
| `rcCenter` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `useGrossPrices` | boolean |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `POST /c/:company_id/receipts` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-receipt.md) for the provider-specific parameters and requirements.


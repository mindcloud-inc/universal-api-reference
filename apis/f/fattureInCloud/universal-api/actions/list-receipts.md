# Fatture in Cloud: List Receipts

Retrieves receipts from Fatture in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-receipts?${params}`, {
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
| `companyId` | number | yes | The ID of the company. |
| `fields` | string | no | List of comma-separated fields. |
| `fieldset` | list | no | Name of the fieldset. One of: `basic`, `detailed`, `fic_view`. |
| `q` | string | no | Query for filtering the results. |

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

Through the native Fatture in Cloud API, this operation is `GET /c/:company_id/receipts` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-receipts.md) for the provider-specific parameters and requirements.


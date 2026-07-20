# Farmbrite: Create transaction

Creates a new transaction in Farmbrite.

```
POST https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "category": "string",
  "amount": 1,
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "category": "string",
    "amount": 1,
    "date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes |  |
| `category` | string | yes |  |
| `amount` | number | yes |  |
| `date` | date | yes |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCode": "string",
      "amount": 1,
      "category": "string",
      "checkNumber": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdById": "string",
      "customFields": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isParent": true,
      "keywords": "string",
      "parentTransactionId": "string",
      "referenceId": "string",
      "referenceType": "string",
      "refId": "string",
      "refType": "string",
      "reportingYear": 1,
      "sourceId": "string",
      "sourceType": "string",
      "taxLine": "string",
      "transactionCategoryId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vendor": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCode` | string |  |
| `amount` | number |  |
| `category` | string |  |
| `checkNumber` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdById` | string |  |
| `customFields` | string |  |
| `date` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isParent` | boolean |  |
| `keywords` | string |  |
| `parentTransactionId` | string |  |
| `referenceId` | string |  |
| `referenceType` | string |  |
| `refId` | string |  |
| `refType` | string |  |
| `reportingYear` | number |  |
| `sourceId` | string |  |
| `sourceType` | string |  |
| `taxLine` | string |  |
| `transactionCategoryId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `vendor` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `POST /transactions` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.


# Farmbrite: Retrieve transaction

Retrieves a specific transaction from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-transaction?${params}`, {
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
| `transactionId` | string | yes |  |

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

Through the native Farmbrite API, this operation is `GET /transactions/:transaction_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-transaction.md) for the provider-specific parameters and requirements.


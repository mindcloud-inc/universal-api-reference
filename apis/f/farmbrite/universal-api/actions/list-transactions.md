# Farmbrite: List transactions

Retrieves a list of transactions from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-transactions?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
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
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].accountCode` | string |  |
| `data[].amount` | number |  |
| `data[].category` | string |  |
| `data[].checkNumber` | string |  |
| `data[].createdAt` | date |  |
| `data[].createdBy` | string |  |
| `data[].createdById` | string |  |
| `data[].customFields` | string |  |
| `data[].date` | date |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].isParent` | boolean |  |
| `data[].keywords` | string |  |
| `data[].parentTransactionId` | string |  |
| `data[].referenceId` | string |  |
| `data[].referenceType` | string |  |
| `data[].refId` | string |  |
| `data[].refType` | string |  |
| `data[].reportingYear` | number |  |
| `data[].sourceId` | string |  |
| `data[].sourceType` | string |  |
| `data[].taxLine` | string |  |
| `data[].transactionCategoryId` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | date |  |
| `data[].vendor` | string |  |
| `data[].year` | number |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /transactions` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.


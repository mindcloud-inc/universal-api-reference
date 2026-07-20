# Peach: List Transactions By Campaign

Retrieves transaction records from Peach by campaign ID.

```
GET https://connect.mindcloud.co/v1/universal/peach/latest/actions/list-transactions-by-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/list-transactions-by-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peach/latest/actions/list-transactions-by-campaign?${params}`, {
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
| `campaignId` | string | yes | Campaign ID to filter transactions. |
| `startDate` | date | no | Start date for retrieving transactions. |
| `endDate` | date | no | End date for retrieving transactions. |
| `limit` | number | no | Maximum rows to return. Peach allows up to 1000. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paginationKey` | object | no | Pagination cursor object from a previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paginationKey": {
        "accountId": "string",
        "transactionDate": 1,
        "transactionId": "string"
      },
      "results": [
        {
          "amount": 1,
          "campaignId": "string",
          "category": "string",
          "contactId": "string",
          "currency": "string",
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "firstName": "Ava",
          "isCancelled": true,
          "isCompleted": true,
          "lastName": "Chen",
          "paymentMethod": "string",
          "paymentType": "string",
          "receiptNumber": 1,
          "receiptUrl": "https://example.com",
          "status": "string",
          "sum": 1,
          "transactionDate": "2026-05-07T12:00:00.000Z",
          "transactionId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paginationKey` | object | Cursor payload for the next page of results when present. |
| `paginationKey.accountId` | string |  |
| `paginationKey.transactionDate` | number |  |
| `paginationKey.transactionId` | string |  |
| `results` | array<object> | Transaction rows returned by the search endpoint. |
| `results[].amount` | number |  |
| `results[].campaignId` | string |  |
| `results[].category` | string |  |
| `results[].contactId` | string |  |
| `results[].currency` | string |  |
| `results[].displayName` | string |  |
| `results[].email` | string |  |
| `results[].firstName` | string |  |
| `results[].isCancelled` | boolean |  |
| `results[].isCompleted` | boolean |  |
| `results[].lastName` | string |  |
| `results[].paymentMethod` | string |  |
| `results[].paymentType` | string |  |
| `results[].receiptNumber` | number |  |
| `results[].receiptUrl` | string |  |
| `results[].status` | string |  |
| `results[].sum` | number |  |
| `results[].transactionDate` | date |  |
| `results[].transactionId` | string |  |

## Native endpoint

Through the native Peach API, this operation is `POST /transactions/search` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions-by-campaign.md) for the provider-specific parameters and requirements.


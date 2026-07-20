# Column: List Book Transfers



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/list-book-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-book-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/list-book-transfers?${params}`, {
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
| `senderBankAccountId` | string | no | Filter book transfers by sender bank account. |
| `receiverBankAccountId` | string | no | Filter book transfers by receiver bank account. |
| `status` | string | no | Filter book transfers by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "transfers": [
        {
          "allowOverdraft": true,
          "amount": 1,
          "createdAt": "string",
          "currencyCode": "string",
          "description": "string",
          "id": "string",
          "idempotencyKey": "string",
          "receiverAccountNumberId": "string",
          "receiverBankAccountId": "string",
          "senderAccountNumberId": "string",
          "senderBankAccountId": "string",
          "status": "string",
          "updatedAt": "string"
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
| `hasMore` | boolean |  |
| `transfers[].allowOverdraft` | boolean |  |
| `transfers[].amount` | number |  |
| `transfers[].createdAt` | string |  |
| `transfers[].currencyCode` | string |  |
| `transfers[].description` | string |  |
| `transfers[].id` | string |  |
| `transfers[].idempotencyKey` | string |  |
| `transfers[].receiverAccountNumberId` | string |  |
| `transfers[].receiverBankAccountId` | string |  |
| `transfers[].senderAccountNumberId` | string |  |
| `transfers[].senderBankAccountId` | string |  |
| `transfers[].status` | string |  |
| `transfers[].updatedAt` | string |  |

## Native endpoint

Through the native Column API, this operation is `GET /transfers/book` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-book-transfers.md) for the provider-specific parameters and requirements.


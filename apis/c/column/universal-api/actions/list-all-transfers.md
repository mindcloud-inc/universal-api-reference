# Column: List All Transfers



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/list-all-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-all-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/list-all-transfers?${params}`, {
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
| `type` | string | no | Transfer type filter; accepts comma-separated values. |
| `bankAccountId` | string | no | Filter transfers touching this bank account. |
| `counterpartyId` | string | no | Filter transfers associated with this counterparty. |
| `transferId` | string | no | Filter results to a specific transfer ID. |
| `status` | string | no | Filter by transfer status; accepts comma-separated values. |
| `isIncoming` | boolean | no | Whether to return incoming or outgoing transfers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "totalResultsCount": 1,
      "transfers": [
        {
          "amount": 1,
          "completedAt": "string",
          "createdAt": "string",
          "currencyCode": "string",
          "description": "string",
          "externalDestination": {
            "counterpartyId": "string"
          },
          "id": "string",
          "idempotencyKey": "string",
          "isIncoming": true,
          "senderInternalAccount": {
            "accountNumberId": "string",
            "bankAccountId": "string"
          },
          "settledAt": {},
          "status": "string",
          "type": "string",
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
| `totalResultsCount` | number |  |
| `transfers[].amount` | number |  |
| `transfers[].completedAt` | string |  |
| `transfers[].createdAt` | string |  |
| `transfers[].currencyCode` | string |  |
| `transfers[].description` | string |  |
| `transfers[].externalDestination.counterpartyId` | string |  |
| `transfers[].id` | string |  |
| `transfers[].idempotencyKey` | string |  |
| `transfers[].isIncoming` | boolean |  |
| `transfers[].senderInternalAccount.accountNumberId` | string |  |
| `transfers[].senderInternalAccount.bankAccountId` | string |  |
| `transfers[].settledAt` | object |  |
| `transfers[].status` | string |  |
| `transfers[].type` | string |  |
| `transfers[].updatedAt` | string |  |

## Native endpoint

Through the native Column API, this operation is `GET /transfers` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-transfers.md) for the provider-specific parameters and requirements.


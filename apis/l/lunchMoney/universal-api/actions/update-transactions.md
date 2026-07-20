# Lunch Money: Update multiple transactions



```
PUT https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-transactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-transactions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactions[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "categoryId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customMetadata": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "files": [
        {}
      ],
      "groupParentId": "string",
      "id": 1,
      "isGroupParent": true,
      "isPending": true,
      "isSplitParent": true,
      "manualAccountId": 1,
      "notes": "string",
      "originalName": "Ava Chen",
      "payee": "string",
      "plaidAccountId": "string",
      "plaidMetadata": "string",
      "recurringId": "string",
      "source": "string",
      "splitParentId": "string",
      "status": "string",
      "tagIds": [
        1
      ],
      "toBase": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `categoryId` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customMetadata` | string |  |
| `date` | date |  |
| `externalId` | string |  |
| `files` | array<object> |  |
| `groupParentId` | string |  |
| `id` | number |  |
| `isGroupParent` | boolean |  |
| `isPending` | boolean |  |
| `isSplitParent` | boolean |  |
| `manualAccountId` | number |  |
| `notes` | string |  |
| `originalName` | string |  |
| `payee` | string |  |
| `plaidAccountId` | string |  |
| `plaidMetadata` | string |  |
| `recurringId` | string |  |
| `source` | string |  |
| `splitParentId` | string |  |
| `status` | string |  |
| `tagIds` | array<number> |  |
| `toBase` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunch Money API, this operation is `PUT /transactions` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transactions.md) for the provider-specific parameters and requirements.


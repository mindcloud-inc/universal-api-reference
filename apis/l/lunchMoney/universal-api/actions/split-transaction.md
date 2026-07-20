# Lunch Money: Split a transaction



```
PUT https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/split-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/split-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "child_transactions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/split-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "child_transactions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `child_transactions[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "categoryId": 1,
      "children": {
        "amount": "string",
        "categoryId": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "date": "2026-05-07T12:00:00.000Z",
        "files": [
          {}
        ],
        "id": 1,
        "isGroupParent": true,
        "isPending": true,
        "isSplitParent": true,
        "manualAccountId": 1,
        "notes": "string",
        "payee": "string",
        "source": "string",
        "splitParentId": 1,
        "status": "string",
        "tagIds": [
          {}
        ],
        "toBase": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
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
| `children` | array<object> |  |
| `children.amount` | string |  |
| `children.categoryId` | number |  |
| `children.createdAt` | date |  |
| `children.currency` | string |  |
| `children.date` | date |  |
| `children.files` | array<object> |  |
| `children.id` | number |  |
| `children.isGroupParent` | boolean |  |
| `children.isPending` | boolean |  |
| `children.isSplitParent` | boolean |  |
| `children.manualAccountId` | number |  |
| `children.notes` | string |  |
| `children.payee` | string |  |
| `children.source` | string |  |
| `children.splitParentId` | number |  |
| `children.status` | string |  |
| `children.tagIds` | array<object> |  |
| `children.toBase` | number |  |
| `children.updatedAt` | date |  |
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

Through the native Lunch Money API, this operation is `POST /transactions/split/:id` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-transaction.md) for the provider-specific parameters and requirements.


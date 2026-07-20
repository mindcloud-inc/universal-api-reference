# Lunch Money: Update an existing transaction



```
PUT https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `notes` | string | no |  |
| `payee` | string | no |  |

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
      "files": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen",
        "notes": "string",
        "size": 1,
        "type": "string",
        "uploadedBy": 1
      },
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
| `files.createdAt` | date |  |
| `files.id` | number |  |
| `files.name` | string |  |
| `files.notes` | string |  |
| `files.size` | number |  |
| `files.type` | string |  |
| `files.uploadedBy` | number |  |
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

Through the native Lunch Money API, this operation is `PUT /transactions/:id` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transaction.md) for the provider-specific parameters and requirements.


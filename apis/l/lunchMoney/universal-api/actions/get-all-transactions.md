# Lunch Money: Get all transactions



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-transactions?${params}`, {
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
| `start_date` | string | no |  |
| `end_date` | string | no |  |
| `include_files` | boolean | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

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
| `recurringId` | string |  |
| `source` | string |  |
| `splitParentId` | string |  |
| `status` | string |  |
| `tagIds` | array<number> |  |
| `toBase` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /transactions` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-transactions.md) for the provider-specific parameters and requirements.


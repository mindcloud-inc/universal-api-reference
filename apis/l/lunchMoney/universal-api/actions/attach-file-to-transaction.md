# Lunch Money: Attach a file to a transaction



```
POST https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/attach-file-to-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/attach-file-to-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transaction_id": 1,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/attach-file-to-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transaction_id": 1,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transaction_id` | number | yes |  |
| `file` | file | yes |  |
| `notes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "size": 1,
      "type": "string",
      "uploadedBy": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `size` | number |  |
| `type` | string |  |
| `uploadedBy` | number |  |

## Native endpoint

Through the native Lunch Money API, this operation is `POST /transactions/:transaction_id/attachments` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-file-to-transaction.md) for the provider-specific parameters and requirements.


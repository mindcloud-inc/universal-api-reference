# Lunch Money: Get all manual accounts



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-manual-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-manual-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-manual-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "balanceAsOf": "2026-05-07T12:00:00.000Z",
      "closedOn": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByName": "Ava Chen",
      "currency": "string",
      "customMetadata": "string",
      "displayName": "Ava Chen",
      "excludeFromTransactions": true,
      "externalId": "string",
      "id": 1,
      "institutionName": "Ava Chen",
      "name": "Ava Chen",
      "status": "string",
      "subtype": "string",
      "toBase": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `balanceAsOf` | date |  |
| `closedOn` | string |  |
| `createdAt` | date |  |
| `createdByName` | string |  |
| `currency` | string |  |
| `customMetadata` | string |  |
| `displayName` | string |  |
| `excludeFromTransactions` | boolean |  |
| `externalId` | string |  |
| `id` | number |  |
| `institutionName` | string |  |
| `name` | string |  |
| `status` | string |  |
| `subtype` | string |  |
| `toBase` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /manual_accounts` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-manual-accounts.md) for the provider-specific parameters and requirements.


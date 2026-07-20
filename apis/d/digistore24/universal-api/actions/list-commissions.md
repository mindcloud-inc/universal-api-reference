# Digistore24: List Commissions

Retrieves a list of commission amounts from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-commissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-commissions?${params}`, {
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
| `from` | string | no | Start date/time |
| `to` | string | no | End date/time |
| `pageNo` | number | no | Page number |
| `pageSize` | number | no | Page size |
| `transactionType` | string | no | Transaction type |
| `commissionType` | string | no | Commission type |
| `purchaseId` | string | no | Purchase ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "purchaseId": "string",
      "reason": "string",
      "schedulePayoutAt": "2026-05-07T12:00:00.000Z",
      "transactionId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Commission amount |
| `createdAt` | date | Creation timestamp |
| `currency` | string | Currency code |
| `id` | number | Commission ID |
| `purchaseId` | string | Purchase ID |
| `reason` | string | Commission reason |
| `schedulePayoutAt` | date | Scheduled payout date |
| `transactionId` | number | Transaction ID |

## Native endpoint

Through the native Digistore24 API, this operation is `GET /listCommissions` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-commissions.md) for the provider-specific parameters and requirements.


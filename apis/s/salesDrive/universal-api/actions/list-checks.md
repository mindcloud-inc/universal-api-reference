# SalesDrive: List Checks

Retrieves a list of checks from SalesDrive.

```
GET https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-checks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-checks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-checks?${params}`, {
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
      "cashier": {},
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "documentPaymentTypeId": 1,
      "fiscalCode": "string",
      "fiscalizationStatus": "string",
      "fiscalizationUserId": 1,
      "hasReturn": 1,
      "id": 1,
      "organization": {},
      "payerTypeId": 1,
      "responsibleId": 1,
      "return": 1,
      "totalSum": 1,
      "type": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cashier` | object |  |
| `comment` | string |  |
| `createdAt` | date |  |
| `date` | date |  |
| `documentPaymentTypeId` | number |  |
| `fiscalCode` | string |  |
| `fiscalizationStatus` | string |  |
| `fiscalizationUserId` | number |  |
| `hasReturn` | number |  |
| `id` | number |  |
| `organization` | object |  |
| `payerTypeId` | number |  |
| `responsibleId` | number |  |
| `return` | number |  |
| `totalSum` | number |  |
| `type` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native SalesDrive API, this operation is `GET /api/check/list/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checks.md) for the provider-specific parameters and requirements.


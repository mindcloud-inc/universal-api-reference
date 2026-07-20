# Syncro: List Estimates

Retrieves a list of estimates from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-estimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-estimates?${params}`, {
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
| `mine` | boolean | no |  |
| `status` | string | no |  |
| `page` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerBusinessThenName": "Ava Chen",
      "customerId": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "employee": "string",
      "id": 1,
      "invoiceId": 1,
      "locationId": 1,
      "name": "Ava Chen",
      "number": "string",
      "pdfUrl": "https://example.com",
      "status": "string",
      "subtotal": "string",
      "tax": "string",
      "ticketId": 1,
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customerBusinessThenName` | string |  |
| `customerId` | number |  |
| `date` | date |  |
| `employee` | string |  |
| `id` | number |  |
| `invoiceId` | number |  |
| `locationId` | number |  |
| `name` | string |  |
| `number` | string |  |
| `pdfUrl` | string |  |
| `status` | string |  |
| `subtotal` | string |  |
| `tax` | string |  |
| `ticketId` | number |  |
| `total` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /estimates` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.


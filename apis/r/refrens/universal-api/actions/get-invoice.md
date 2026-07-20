# Refrens: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/refrens/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refrens/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes | Refrens invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "billedBy": {},
      "billedTo": {},
      "billType": "string",
      "client": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "finalTotal": {},
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceNumber": "string",
      "invoiceTitle": "string",
      "items": [
        {}
      ],
      "share": {},
      "status": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `billedBy` | object |  |
| `billedTo` | object |  |
| `billType` | string |  |
| `client` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `finalTotal` | object |  |
| `invoiceDate` | date |  |
| `invoiceNumber` | string |  |
| `invoiceTitle` | string |  |
| `items` | array<object> |  |
| `share` | object |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Refrens API, this operation is `GET /businesses/:urlKey/invoices/:invoiceId` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.


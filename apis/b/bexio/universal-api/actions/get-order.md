# Bexio: Get Order

Retrieves an order from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-order?${params}`, {
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
| `orderId` | number | yes | The ID of the order. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiReference": "string",
      "bankAccountId": 1,
      "contactAddress": "string",
      "contactId": 1,
      "contactSubId": {},
      "currencyId": 1,
      "deliveryAddress": "string",
      "deliveryAddressType": 1,
      "documentNr": "string",
      "footer": "string",
      "header": "string",
      "id": 1,
      "isRecurring": true,
      "isValidFrom": "2026-05-07T12:00:00.000Z",
      "kbItemStatusId": 1,
      "languageId": 1,
      "logopaperId": 1,
      "mwstIsNet": true,
      "mwstType": 1,
      "networkLink": "https://example.com",
      "paymentTypeId": 1,
      "positions": [
        {
          "id": 1,
          "internalPos": 1,
          "isOptional": true,
          "parentId": {},
          "pos": {},
          "showPosNr": true,
          "text": "string",
          "type": "string"
        }
      ],
      "projectId": {},
      "showPositionTaxes": true,
      "templateSlug": "string",
      "title": "string",
      "total": "string",
      "totalGross": "string",
      "totalNet": "string",
      "totalRoundingDifference": 1,
      "totalTaxes": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "viewedByClientAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiReference` | string |  |
| `bankAccountId` | number |  |
| `contactAddress` | string |  |
| `contactId` | number |  |
| `contactSubId` | object |  |
| `currencyId` | number |  |
| `deliveryAddress` | string |  |
| `deliveryAddressType` | number |  |
| `documentNr` | string |  |
| `footer` | string |  |
| `header` | string |  |
| `id` | number |  |
| `isRecurring` | boolean |  |
| `isValidFrom` | date |  |
| `kbItemStatusId` | number |  |
| `languageId` | number |  |
| `logopaperId` | number |  |
| `mwstIsNet` | boolean |  |
| `mwstType` | number |  |
| `networkLink` | string |  |
| `paymentTypeId` | number |  |
| `positions[].id` | number |  |
| `positions[].internalPos` | number |  |
| `positions[].isOptional` | boolean |  |
| `positions[].parentId` | object |  |
| `positions[].pos` | object |  |
| `positions[].showPosNr` | boolean |  |
| `positions[].text` | string |  |
| `positions[].type` | string |  |
| `projectId` | object |  |
| `showPositionTaxes` | boolean |  |
| `templateSlug` | string |  |
| `title` | string |  |
| `total` | string |  |
| `totalGross` | string |  |
| `totalNet` | string |  |
| `totalRoundingDifference` | number |  |
| `totalTaxes` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `viewedByClientAt` | date |  |

## Native endpoint

Through the native Bexio API, this operation is `GET /2.0/kb_order/:order_id` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.


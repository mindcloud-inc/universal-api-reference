# Zenvoices: Get Purchase Order

Retrieves a purchase order from Zenvoices by purchase order number.

```
GET https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenvoices `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/get-purchase-order?${params}`, {
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
      "accountCode": "string",
      "administrationId": 1,
      "currencyCode": "string",
      "description": "string",
      "externalId": "string",
      "lines": [
        "string"
      ],
      "purchaseDate": "2026-05-07T12:00:00.000Z",
      "purchaseOrderNumber": "string",
      "taxExclusiveAmount": 1,
      "taxInclusiveAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCode` | string | accountCode returned by Zenvoices. |
| `administrationId` | number | administrationId returned by Zenvoices. |
| `currencyCode` | string | currencyCode returned by Zenvoices. |
| `description` | string | description returned by Zenvoices. |
| `externalId` | string | externalId returned by Zenvoices. |
| `lines` | array | lines returned by Zenvoices. |
| `purchaseDate` | date | purchaseDate returned by Zenvoices. |
| `purchaseOrderNumber` | string | purchaseOrderNumber returned by Zenvoices. |
| `taxExclusiveAmount` | number | taxExclusiveAmount returned by Zenvoices. |
| `taxInclusiveAmount` | number | taxInclusiveAmount returned by Zenvoices. |

## Native endpoint

Through the native Zenvoices API, this operation is `GET /public-api/v1/purchaseOrders` (base URL `https://app.zenvoices.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.


# Evoliz: Update Invoice

Updates an existing invoice in Evoliz.

```
PUT https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | The Evoliz invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "clientid": 1,
        "code": "string",
        "name": "Ava Chen"
      },
      "default_currency": {
        "code": "string",
        "symbol": "string"
      },
      "document_number": "string",
      "documentdate": "2026-05-07T12:00:00.000Z",
      "duedate": "2026-05-07T12:00:00.000Z",
      "file": "string",
      "invoiceid": 1,
      "items": [
        {
          "articleid": 1,
          "designation": "string",
          "itemid": 1,
          "quantity": 1,
          "reference": "string",
          "unit_price_vat_exclude": 1,
          "vat": 1
        }
      ],
      "links": "https://example.com",
      "locked": 1,
      "object": "string",
      "prices_include_vat": true,
      "recovery_number": 1,
      "status": "string",
      "status_code": 1,
      "template": {
        "label": "string",
        "templateid": 1
      },
      "total": {
        "advance": 1,
        "net_to_pay": 1,
        "paid": 1,
        "vat": 1,
        "vat_exclude": 1,
        "vat_include": 1
      },
      "typedoc": "string",
      "userid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client.clientid` | number |  |
| `client.code` | string |  |
| `client.name` | string |  |
| `default_currency.code` | string |  |
| `default_currency.symbol` | string |  |
| `document_number` | string |  |
| `documentdate` | date |  |
| `duedate` | date |  |
| `file` | string |  |
| `invoiceid` | number |  |
| `items[].articleid` | number |  |
| `items[].designation` | string |  |
| `items[].itemid` | number |  |
| `items[].quantity` | number |  |
| `items[].reference` | string |  |
| `items[].unit_price_vat_exclude` | number |  |
| `items[].vat` | number |  |
| `links` | string |  |
| `locked` | number |  |
| `object` | string |  |
| `prices_include_vat` | boolean |  |
| `recovery_number` | number |  |
| `status` | string |  |
| `status_code` | number |  |
| `template.label` | string |  |
| `template.templateid` | number |  |
| `total.advance` | number |  |
| `total.net_to_pay` | number |  |
| `total.paid` | number |  |
| `total.vat` | number |  |
| `total.vat_exclude` | number |  |
| `total.vat_include` | number |  |
| `typedoc` | string |  |
| `userid` | number |  |

## Native endpoint

Through the native Evoliz API, this operation is `PUT /api/v1/invoices/:invoiceid` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.


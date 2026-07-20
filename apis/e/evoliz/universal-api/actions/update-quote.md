# Evoliz: Update Quote

Updates an existing quote in Evoliz.

```
PUT https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/update-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/update-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quoteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/update-quote', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quoteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | number | yes | The Evoliz quote ID. |

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
      "object": "string",
      "organization": "string",
      "prices_include_vat": true,
      "quoteid": 1,
      "status": "string",
      "status_code": 1,
      "status_dates": {
        "create": "2026-05-07T12:00:00.000Z"
      },
      "template": {
        "label": "string",
        "templateid": 1
      },
      "total": {
        "net_to_pay": 1,
        "vat": 1,
        "vat_exclude": 1,
        "vat_include": 1
      },
      "userid": 1,
      "webdoc": "string"
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
| `items[].articleid` | number |  |
| `items[].designation` | string |  |
| `items[].itemid` | number |  |
| `items[].quantity` | number |  |
| `items[].reference` | string |  |
| `items[].unit_price_vat_exclude` | number |  |
| `items[].vat` | number |  |
| `links` | string |  |
| `object` | string |  |
| `organization` | string |  |
| `prices_include_vat` | boolean |  |
| `quoteid` | number |  |
| `status` | string |  |
| `status_code` | number |  |
| `status_dates.create` | date |  |
| `template.label` | string |  |
| `template.templateid` | number |  |
| `total.net_to_pay` | number |  |
| `total.vat` | number |  |
| `total.vat_exclude` | number |  |
| `total.vat_include` | number |  |
| `userid` | number |  |
| `webdoc` | string |  |

## Native endpoint

Through the native Evoliz API, this operation is `PUT /api/v1/quotes/:quoteid` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-quote.md) for the provider-specific parameters and requirements.


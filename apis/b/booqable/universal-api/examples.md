# Booqable Universal API Examples

These examples use the MindCloud API key and Booqable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Items

Retrieves item records from Booqable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "allowShortage": true,
        "archived": true,
        "basePriceInCents": 1,
        "bufferTimeAfter": 1,
        "bufferTimeBefore": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultPurchaseCostInCents": 1,
        "depositInCents": 1,
        "description": "string",
        "discountable": true,
        "extraInformation": "string",
        "groupName": "Ava Chen",
        "hasVariations": true,
        "name": "Ava Chen",
        "photoId": "string",
        "pricePeriod": "string",
        "priceType": "string",
        "productType": "string",
        "properties": {},
        "shortageLimit": 1,
        "showInStore": true,
        "sku": "string",
        "slug": "string",
        "sortingWeight": 1,
        "tagList": [
          "string"
        ],
        "taxable": true,
        "taxCategoryId": "string",
        "trackable": true,
        "trackingType": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "variation": true
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Items action reference](actions/list-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/booqable/latest/actions/list-items).

## Create Customer

Creates a new customer in Booqable.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/booqable/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archived": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "depositType": "string",
        "depositValue": 1,
        "discountPercentage": 1,
        "email": "ava@example.com",
        "legalType": "string",
        "name": "Ava Chen",
        "number": 1,
        "orderCount": 1,
        "properties": {},
        "tagList": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/booqable/latest/actions/create-customer).

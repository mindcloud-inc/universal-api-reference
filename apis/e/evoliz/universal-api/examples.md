# Evoliz Universal API Examples

These examples use the MindCloud API key and Evoliz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Article

Retrieves an article from Evoliz.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/get-article?connectionId=$CONNECTION_ID&articleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/get-article?${params}`, {
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
      "articleid": 1,
      "designation": "string",
      "enabled": true,
      "picture_link": "https://example.com",
      "quantity": 1,
      "reference": "string",
      "sale_classification": {
        "code": "string",
        "id": 1,
        "label": "string"
      },
      "stock_management": true,
      "stocked_quantity": 1,
      "ttc": true,
      "unit_price_vat_exclude": 1,
      "unit_price_vat_include": 1,
      "userid": 1,
      "vat": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Article action reference](actions/get-article.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evoliz/latest/actions/get-article).

## Create Client

Creates a new client in Evoliz.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/create-client', {
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
      "address": {
        "country": {
          "iso2": "string",
          "label": "string"
        },
        "postcode": "string",
        "town": "string"
      },
      "clientid": 1,
      "code": "string",
      "comment": "string",
      "enabled": true,
      "name": "Ava Chen",
      "phone": "string",
      "safe_amount": 1,
      "stampdate": "2026-05-07T12:00:00.000Z",
      "ttc": true,
      "type": "string",
      "userid": 1,
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/evoliz/latest/actions/create-client).

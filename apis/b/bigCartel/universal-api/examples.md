# Big Cartel Universal API Examples

These examples use the MindCloud API key and Big Cartel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from Big Cartel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-account?${params}`, {
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
        "artistsEnabled": true,
        "contactEmail": "ava@example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "firstName": "Ava",
        "hasActiveAdvancedTaxSettings": true,
        "inventoryEnabled": true,
        "lastName": "Chen",
        "launched": true,
        "storeName": "Ava Chen",
        "subdomain": "string",
        "timeZone": "string",
        "underMaintenance": true,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      },
      "id": "string",
      "relationships": {
        "categories": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "country": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "currency": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "discounts": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "orders": {
          "links": {
            "related": "https://example.com"
          }
        },
        "plan": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "products": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigCartel/latest/actions/get-account).

## Create Category

Creates a category in Big Cartel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "name": "Ava Chen"
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
        "name": "Ava Chen",
        "permalink": "https://example.com",
        "position": 1
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Category action reference](actions/create-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigCartel/latest/actions/create-category).

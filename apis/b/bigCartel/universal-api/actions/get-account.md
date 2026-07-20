# Big Cartel: Get Account

Retrieves account details from Big Cartel.

```
GET https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.artistsEnabled` | boolean |  |
| `attributes.contactEmail` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.firstName` | string |  |
| `attributes.hasActiveAdvancedTaxSettings` | boolean |  |
| `attributes.inventoryEnabled` | boolean |  |
| `attributes.lastName` | string |  |
| `attributes.launched` | boolean |  |
| `attributes.storeName` | string |  |
| `attributes.subdomain` | string |  |
| `attributes.timeZone` | string |  |
| `attributes.underMaintenance` | boolean |  |
| `attributes.updatedAt` | date |  |
| `attributes.url` | string |  |
| `id` | string |  |
| `relationships.categories.links.related` | string |  |
| `relationships.categories.links.self` | string |  |
| `relationships.country.data.id` | string |  |
| `relationships.country.data.type` | string |  |
| `relationships.currency.data.id` | string |  |
| `relationships.currency.data.type` | string |  |
| `relationships.discounts.links.related` | string |  |
| `relationships.discounts.links.self` | string |  |
| `relationships.orders.links.related` | string |  |
| `relationships.plan.data.id` | string |  |
| `relationships.plan.data.type` | string |  |
| `relationships.products.links.related` | string |  |
| `relationships.products.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `GET /v1/accounts` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.


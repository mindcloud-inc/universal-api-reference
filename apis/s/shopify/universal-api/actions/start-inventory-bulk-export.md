# Shopify: Start Inventory Bulk Export



```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/start-inventory-bulk-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/start-inventory-bulk-export?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/start-inventory-bulk-export?${params}`, {
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
      "data": {
        "bulkOperationRunQuery": {
          "bulkOperation": {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "status": "string"
          }
        }
      },
      "extensions": {
        "cost": {
          "actualQueryCost": 1,
          "requestedQueryCost": 1,
          "throttleStatus": {
            "currentlyAvailable": 1,
            "maximumAvailable": 1,
            "restoreRate": 1
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.bulkOperationRunQuery.bulkOperation.createdAt` | date |  |
| `data.bulkOperationRunQuery.bulkOperation.id` | string |  |
| `data.bulkOperationRunQuery.bulkOperation.status` | string |  |
| `extensions.cost.actualQueryCost` | number |  |
| `extensions.cost.requestedQueryCost` | number |  |
| `extensions.cost.throttleStatus.currentlyAvailable` | number |  |
| `extensions.cost.throttleStatus.maximumAvailable` | number |  |
| `extensions.cost.throttleStatus.restoreRate` | number |  |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-inventory-bulk-export.md) for the provider-specific parameters and requirements.


# Cliniko: List Billable Items

Retrieves billable items from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-billable-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-billable-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-billable-items?${params}`, {
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
      "billableItems": [
        {
          "archivedAt": {},
          "concessionPrices": {
            "links": {
              "self": "https://example.com"
            }
          },
          "createdAt": "string",
          "id": "string",
          "itemCode": {},
          "itemType": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "price": "string",
          "updatedAt": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "totalEntries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableItems[].archivedAt` | object |  |
| `billableItems[].concessionPrices.links.self` | string |  |
| `billableItems[].createdAt` | string |  |
| `billableItems[].id` | string |  |
| `billableItems[].itemCode` | object |  |
| `billableItems[].itemType` | string |  |
| `billableItems[].links.self` | string |  |
| `billableItems[].name` | string |  |
| `billableItems[].price` | string |  |
| `billableItems[].updatedAt` | string |  |
| `links.self` | string |  |
| `totalEntries` | number |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /billable_items` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-billable-items.md) for the provider-specific parameters and requirements.


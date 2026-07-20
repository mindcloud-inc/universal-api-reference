# Emporix Commerce Engine: List Price Lists

Retrieves price lists from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-price-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-price-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-price-lists?${params}`, {
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
      "countries": [
        "string"
      ],
      "currency": "string",
      "customerGroups": [
        {}
      ],
      "id": "string",
      "legalEntityId": "string",
      "metadata": {},
      "name": {},
      "regions": [
        "string"
      ],
      "siteCode": "string",
      "validity": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries` | array<string> |  |
| `currency` | string |  |
| `customerGroups` | array<object> |  |
| `id` | string |  |
| `legalEntityId` | string |  |
| `metadata` | object |  |
| `name` | object |  |
| `regions` | array<string> |  |
| `siteCode` | string |  |
| `validity` | object |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /price/{{credentials.tenantId}}/price-lists` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-price-lists.md) for the provider-specific parameters and requirements.


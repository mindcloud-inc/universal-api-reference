# AdvantShop: Get Search Filter

Retrieves search filters from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-search-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-search-filter?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-search-filter?${params}`, {
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
      "brands": [
        {}
      ],
      "colors": [
        {}
      ],
      "price": {},
      "properties": [
        {}
      ],
      "sizes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brands` | array<object> |  |
| `colors` | array<object> |  |
| `price` | object |  |
| `properties` | array<object> |  |
| `sizes` | array<object> |  |

## Native endpoint

Through the native AdvantShop API, this operation is `POST /search/filter` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-filter.md) for the provider-specific parameters and requirements.


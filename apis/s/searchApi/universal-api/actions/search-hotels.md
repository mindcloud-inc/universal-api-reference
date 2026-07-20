# SearchApi: Search Hotels



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-hotels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-hotels?connectionId=$CONNECTION_ID&q=Hotels%20in%20Manhattan%20New%20York&checkInDate=2026-04-16&checkOutDate=2026-04-23" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Hotels in Manhattan New York",
  "checkInDate": "2026-04-16",
  "checkOutDate": "2026-04-23"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-hotels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | yes | Example: `Hotels in Manhattan New York`. |
| `checkInDate` | string | yes | Example: `2026-04-16`. |
| `checkOutDate` | string | yes | Example: `2026-04-23`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brands": [
        {}
      ],
      "pagination": {},
      "properties": [
        {}
      ],
      "searchInformation": {},
      "searchMetadata": {},
      "searchParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brands` | array<object> |  |
| `pagination` | object |  |
| `properties` | array<object> |  |
| `searchInformation` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-hotels.md) for the provider-specific parameters and requirements.


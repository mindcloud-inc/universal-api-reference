# OneMap SG: Search Locations

Finds locations in OneMap SG by search value.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/search-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/search-locations?connectionId=$CONNECTION_ID&searchVal=200640" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchVal": "200640"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/search-locations?${params}`, {
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
| `searchVal` | string | yes | The search text, address, postal code, or other lookup value to search in OneMap. Example: `200640`. |
| `returnGeom` | string | no | Whether to include geometry values in the search response. Default: `Y`. Example: `Y`. |
| `getAddrDetails` | string | no | Whether to include detailed address fields in the response. Default: `Y`. Example: `Y`. |
| `pageNum` | number | no | The results page number to return. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "found": 1,
      "pageNum": 1,
      "results": [
        {}
      ],
      "totalNumPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `found` | number | The number of matching results returned by OneMap. |
| `pageNum` | number | The current result page number. |
| `results` | array<object> | The matching search results. |
| `totalNumPages` | number | The total number of result pages. |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/common/elastic/search` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-locations.md) for the provider-specific parameters and requirements.


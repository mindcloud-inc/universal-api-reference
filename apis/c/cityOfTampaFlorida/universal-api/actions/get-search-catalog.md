# City of Tampa, Florida: Get Search Catalog

Retrieves the search catalog from City of Tampa, Florida.

```
GET https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-search-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Tampa, Florida `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-search-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-search-catalog?${params}`, {
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
      "collections": [
        {}
      ],
      "schemaVersion": 1,
      "scopes": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<object> |  |
| `schemaVersion` | number |  |
| `scopes` | object |  |
| `title` | string |  |

## Native endpoint

Through the native City of Tampa, Florida API, this operation is `GET https://city-tampa.opendata.arcgis.com/api/search/v1/catalog` (base URL `https://www.tampa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-catalog.md) for the provider-specific parameters and requirements.


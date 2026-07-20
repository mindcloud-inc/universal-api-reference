# City of Tampa, Florida: Get Collection

Retrieves a data collection from City of Tampa, Florida.

```
GET https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Tampa, Florida `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-collection?${params}`, {
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
| `collectionId` | string | yes | Search API collection identifier, for example dataset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "crs": [
        "string"
      ],
      "description": "string",
      "filters": [
        {}
      ],
      "id": "string",
      "itemType": "string",
      "links": [
        {}
      ],
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `crs` | array<string> |  |
| `description` | string |  |
| `filters` | array<object> |  |
| `id` | string |  |
| `itemType` | string |  |
| `links` | array<object> |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native City of Tampa, Florida API, this operation is `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId` (base URL `https://www.tampa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.


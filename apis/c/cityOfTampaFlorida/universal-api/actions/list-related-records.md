# City of Tampa, Florida: List Related Records

Retrieves related records from City of Tampa, Florida.

```
GET https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-related-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Tampa, Florida `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-related-records?connectionId=$CONNECTION_ID&collectionId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-related-records?${params}`, {
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
| `recordId` | string | yes | GeoHub record identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": [
        "string"
      ],
      "links": [
        {}
      ],
      "numberMatched": 1,
      "numberReturned": 1,
      "timestamp": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<string> |  |
| `links` | array<object> |  |
| `numberMatched` | number |  |
| `numberReturned` | number |  |
| `timestamp` | string |  |
| `type` | string |  |

## Native endpoint

Through the native City of Tampa, Florida API, this operation is `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items/:recordId/related` (base URL `https://www.tampa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-related-records.md) for the provider-specific parameters and requirements.


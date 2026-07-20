# HasData: Search Yelp Places

Retrieves Yelp place results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-yelp-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-yelp-places?connectionId=$CONNECTION_ID&keyword=string&location=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string",
  "location": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-yelp-places?${params}`, {
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
| `domain` | string | no | Yelp domain, such as www.yelp.com. |
| `keyword` | string | yes | Search keyword for Yelp businesses. |
| `location` | string | yes | Location to search for Yelp businesses. |
| `start` | string | no | Result offset for Yelp pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {}
      ],
      "organicResults": [
        {}
      ],
      "pagination": {},
      "requestMetadata": {},
      "searchInformation": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> |  |
| `organicResults` | array<object> |  |
| `pagination` | object |  |
| `requestMetadata` | object |  |
| `searchInformation` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/yelp/search` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-yelp-places.md) for the provider-specific parameters and requirements.


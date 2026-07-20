# HasData: Search Google SERP Light

Retrieves Google SERP Light results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-serp-light
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-serp-light?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-serp-light?${params}`, {
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
| `location` | string | no | Google canonical location for the search. |
| `num` | string | no | Number of results to return per page. |
| `q` | string | yes | Search term to send to Google. |
| `start` | string | no | Number of results to skip for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organicResults": [
        {}
      ],
      "relatedSearches": [
        {}
      ],
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
| `organicResults` | array<object> |  |
| `relatedSearches` | array<object> |  |
| `requestMetadata` | object |  |
| `searchInformation` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google-light/serp` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-serp-light.md) for the provider-specific parameters and requirements.


# PeakIDX: List Search Results

Retrieves listings for a saved search in PeakIDX.

```
GET https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/list-search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeakIDX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/list-search-results?connectionId=$CONNECTION_ID&searchEmbedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchEmbedId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/list-search-results?${params}`, {
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
| `searchEmbedId` | string | yes | The saved search embed identifier from the PeakIDX Search Embeds page. |
| `offset` | number | no | Starting position for the results. PeakIDX docs allow values from 0 through 10000. Default: `0`. |
| `limit` | number | no | Maximum number of results to return. PeakIDX docs allow values from 0 through 200. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "listings": [
        [
          {}
        ]
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of listings returned in this response. |
| `listings[]` | array<object> | Listings returned for the requested saved search. |
| `listings[].address` | string | Listing street address. |
| `listings[].baths` | number | Bathroom count. |
| `listings[].beds` | number | Bedroom count. |
| `listings[].city` | string | Listing city. |
| `listings[].listingId` | number | PeakIDX listing identifier. |
| `listings[].price` | number | Listing price. |
| `total` | number | Total number of listings that match the saved search. |

## Native endpoint

Through the native PeakIDX API, this operation is `GET https://{{credentials.siteName}}.peakidxsites.com/search-results-api/:searchEmbedId` (base URL `https://account.peakidxsites.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-search-results.md) for the provider-specific parameters and requirements.


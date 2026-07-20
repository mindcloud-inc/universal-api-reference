# HasData: Search Zillow Listings

Retrieves Zillow listings from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-zillow-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-zillow-listings?connectionId=$CONNECTION_ID&keyword=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-zillow-listings?${params}`, {
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
| `keyword` | string | yes | Location keyword or area for Zillow listings. |
| `page` | number | no | Page number of Zillow listing results. |
| `sort` | string | no | Sort order for Zillow listings. |
| `type` | string | yes | Listing type, such as forSale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "properties": [
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
| `pagination` | object |  |
| `properties` | array<object> |  |
| `requestMetadata` | object |  |
| `searchInformation` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/zillow/listing` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-zillow-listings.md) for the provider-specific parameters and requirements.


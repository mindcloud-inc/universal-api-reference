# HasData: Search Airbnb Listings

Retrieves Airbnb listings from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-airbnb-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-airbnb-listings?connectionId=$CONNECTION_ID&checkIn=string&location=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checkIn": "string",
  "location": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-airbnb-listings?${params}`, {
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
| `checkIn` | string | yes | Check-in date in YYYY-MM-DD format. |
| `checkOut` | string | no | Check-out date in YYYY-MM-DD format. |
| `location` | string | yes | Location to search for Airbnb listings. |
| `nextPageToken` | string | no | Token for the next page of Airbnb listings. |

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
      "requestMetadata": {}
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

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/airbnb/listing` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-airbnb-listings.md) for the provider-specific parameters and requirements.


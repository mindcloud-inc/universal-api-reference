# HasData: Search Indeed Listings

Retrieves Indeed listings from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-indeed-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-indeed-listings?connectionId=$CONNECTION_ID&keyword=string&location=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string",
  "location": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-indeed-listings?${params}`, {
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
| `domain` | string | no | Indeed domain, such as www.indeed.com. |
| `keyword` | string | yes | Job keyword to search on Indeed. |
| `location` | string | yes | Location to search on Indeed. |
| `sort` | string | no | Sort order for Indeed results, such as date. |
| `start` | number | no | Result offset for Indeed pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobs": [
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
| `jobs` | array<object> |  |
| `pagination` | object |  |
| `requestMetadata` | object |  |
| `searchInformation` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/indeed/listing` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-indeed-listings.md) for the provider-specific parameters and requirements.


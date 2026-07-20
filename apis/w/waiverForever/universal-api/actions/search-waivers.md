# WaiverForever: Search Waivers

Finds waivers in WaiverForever by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/search-waivers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/search-waivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/search-waivers?${params}`, {
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
| `endTimestamp` | number | no | End timestamp in seconds. |
| `page` | number | no | Results page number. |
| `perPage` | number | no | Results returned per page. |
| `searchTerm` | string | no | Search keyword. |
| `startTimestamp` | number | no | Start timestamp in seconds. |
| `templateIds` | list<string> | no | Template ids to constrain the search. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "perPage": 1,
      "total": 1,
      "waivers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number | Current search results page. |
| `perPage` | number | Number of waivers returned per page. |
| `total` | number | Total waivers matching the search. |
| `waivers` | array<object> | Waivers matching the search filters. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v1/waiver/search` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-waivers.md) for the provider-specific parameters and requirements.


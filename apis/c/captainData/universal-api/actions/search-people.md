# Captain Data: Search People

Finds people in Captain Data by Sales Navigator query.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/search-people?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/search-people?${params}`, {
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
| `query` | string | yes | Sales Navigator people search query copied from the LinkedIn search URL. |
| `cursor` | string | no | Pagination cursor from the X-Pagination-Next response header. |
| `pageSize` | number | no | Captain Data fixed people-search page size. Leave at the documented default. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "job_end": "string",
      "job_start": "string",
      "job_time_period": "string",
      "job_title": "string",
      "last_name": "Chen",
      "li_company_id": 1,
      "li_profile_id": 1,
      "li_profile_image_url": "https://example.com",
      "li_profile_url": "https://example.com",
      "location": "string",
      "recently_hired": true,
      "recently_promoted": true,
      "summary": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `job_end` | string |  |
| `job_start` | string |  |
| `job_time_period` | string |  |
| `job_title` | string |  |
| `last_name` | string |  |
| `li_company_id` | number |  |
| `li_profile_id` | number |  |
| `li_profile_image_url` | string |  |
| `li_profile_url` | string |  |
| `location` | string |  |
| `recently_hired` | boolean |  |
| `recently_promoted` | boolean |  |
| `summary` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /people/search` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.


# RocketReach: Search People

Finds people in RocketReach.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/search-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/search-people?${params}`, {
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
| `order_by` | string | no | Specifies the ordering of search results. Popularity matches the Search web app ordering. |
| `page_size` | number | no | Maximum number of results to return per page (1-100). |
| `query` | object | no | RocketReach PersonQuery object. Pass any documented people-search filters here, including fields such as name, current_employer, current_title, department, geo, skills, company filters, and other provider-supported nested keys. |
| `query.current_employer[]` | array<string> | no |  |
| `query.name[]` | array<string> | no |  |
| `start` | number | no | Start index of the request results, counting from 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "profiles": [
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
| `pagination` | object | Search pagination metadata returned by RocketReach. |
| `profiles` | array<object> | People search results. |

## Native endpoint

Through the native RocketReach API, this operation is `POST /person/search` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.


# Owen Wilson Wow API: Get Ordered Wow Range



```
GET https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/get-ordered-wow-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Owen Wilson Wow API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/get-ordered-wow-range?connectionId=$CONNECTION_ID&range=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "range": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/get-ordered-wow-range?${params}`, {
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
| `range` | string | yes | Inclusive chronological wow index range, for example 3-7. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "audio": "https://example.com",
          "character": "string",
          "current_wow_in_movie": 1,
          "director": "string",
          "full_line": "string",
          "movie": "string",
          "movie_duration": "string",
          "poster": "https://example.com",
          "release_date": "string",
          "timestamp": "string",
          "total_wows_in_movie": 1,
          "video": {},
          "year": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> | Chronological wow records. |
| `[].audio` | string | Audio URL. |
| `[].character` | string | Owen Wilson character. |
| `[].current_wow_in_movie` | number | Wow occurrence in the movie. |
| `[].director` | string | Movie director. |
| `[].full_line` | string | Full quoted line. |
| `[].movie` | string | Movie title. |
| `[].movie_duration` | string | Movie duration. |
| `[].poster` | string | Movie poster URL. |
| `[].release_date` | string | Movie release date. |
| `[].timestamp` | string | Wow timestamp. |
| `[].total_wows_in_movie` | number | Total wows in the movie. |
| `[].video` | object | Video URLs by resolution. |
| `[].year` | number | Release year. |

## Native endpoint

Through the native Owen Wilson Wow API API, this operation is `GET /wows/ordered/:range` (base URL `https://owen-wilson-wow-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ordered-wow-range.md) for the provider-specific parameters and requirements.


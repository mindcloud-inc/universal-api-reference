# Studio Ghibli: Get Film by ID



```
GET https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-film-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Studio Ghibli `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-film-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-film-by-id?${params}`, {
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
| `id` | string | yes | Resource UUID documented by the provider. |
| `fields` | string | no | Optional comma-separated list of response fields documented by the provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "director": "string",
      "id": "string",
      "image": "string",
      "locations": [
        "string"
      ],
      "movie_banner": "string",
      "original_title": "string",
      "original_title_romanised": "string",
      "people": [
        "string"
      ],
      "producer": "string",
      "release_date": "string",
      "rt_score": "string",
      "running_time": "string",
      "species": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "vehicles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Film description. |
| `director` | string | Director name. |
| `id` | string | Provider UUID. |
| `image` | string | Provider image URL. |
| `locations` | array<string> | Related location URLs. |
| `movie_banner` | string | Provider banner URL. |
| `original_title` | string | Native original-language title. |
| `original_title_romanised` | string | Native romanised title. |
| `people` | array<string> | Related person URLs. |
| `producer` | string | Producer name. |
| `release_date` | string | Provider release-year string. |
| `rt_score` | string | Provider Rotten Tomatoes score string. |
| `running_time` | string | Provider running-time string. |
| `species` | array<string> | Related species URLs. |
| `title` | string | Film title. |
| `url` | string | Canonical resource URL. |
| `vehicles` | array<string> | Related vehicle URLs. |

## Native endpoint

Through the native Studio Ghibli API, this operation is `GET /films/:id` (base URL `https://ghibliapi.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-film-by-id.md) for the provider-specific parameters and requirements.


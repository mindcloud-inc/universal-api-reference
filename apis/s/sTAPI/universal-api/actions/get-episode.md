# STAPI: Get Episode



```
GET https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-episode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-episode?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-episode?${params}`, {
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
| `uid` | string | yes | Episode unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "episode": {
        "episodeNumber": 1,
        "seasonNumber": 1,
        "series": {
          "title": "string"
        },
        "title": "string",
        "uid": "string",
        "usAirDate": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `episode` | object |  |
| `episode.episodeNumber` | number |  |
| `episode.seasonNumber` | number |  |
| `episode.series` | object |  |
| `episode.series.title` | string |  |
| `episode.title` | string |  |
| `episode.uid` | string |  |
| `episode.usAirDate` | string |  |

## Native endpoint

Through the native STAPI API, this operation is `GET /v1/rest/episode` (base URL `https://stapi.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode.md) for the provider-specific parameters and requirements.


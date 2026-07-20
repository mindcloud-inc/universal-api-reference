# OMDb: Get Season by IMDb ID

Retrieves a season from OMDb by series IMDb ID and season.

```
GET https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-season-by-imdb-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OMDb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-season-by-imdb-id?connectionId=$CONNECTION_ID&imdbId=string&season=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imdbId": "string",
  "season": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-season-by-imdb-id?${params}`, {
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
| `imdbId` | string | yes | Series IMDb ID to use for the season lookup. |
| `season` | number | yes | Season number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Episodes": [
        {}
      ],
      "Response": "string",
      "Season": "string",
      "Title": "string",
      "totalSeasons": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Episodes` | array<object> |  |
| `Response` | string |  |
| `Season` | string |  |
| `Title` | string |  |
| `totalSeasons` | string |  |

## Native endpoint

Through the native OMDb API, this operation is `GET /` (base URL `https://www.omdbapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-season-by-imdb-id.md) for the provider-specific parameters and requirements.


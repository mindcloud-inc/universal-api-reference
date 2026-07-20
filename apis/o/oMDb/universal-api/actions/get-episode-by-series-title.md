# OMDb: Get Episode by Series Title

Retrieves an episode from OMDb by series title, season, and episode.

```
GET https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-episode-by-series-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OMDb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-episode-by-series-title?connectionId=$CONNECTION_ID&title=string&season=1&episode=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "string",
  "season": "1",
  "episode": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-episode-by-series-title?${params}`, {
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
| `title` | string | yes | Series title to use for the episode lookup. |
| `season` | number | yes | Season number that contains the episode. |
| `episode` | number | yes | Episode number within the season. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Actors": "string",
      "Awards": "string",
      "BoxOffice": "string",
      "Country": "string",
      "Director": "string",
      "DVD": "string",
      "Episode": "string",
      "Genre": "string",
      "imdbID": "string",
      "imdbRating": "string",
      "imdbVotes": "string",
      "Language": "string",
      "Metascore": "string",
      "Plot": "string",
      "Poster": "string",
      "Production": "string",
      "Rated": "string",
      "Ratings": [
        {}
      ],
      "Released": "string",
      "Response": "string",
      "Runtime": "string",
      "Season": "string",
      "seriesID": "string",
      "Title": "string",
      "totalSeasons": "string",
      "Type": "string",
      "Website": "string",
      "Writer": "string",
      "Year": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Actors` | string |  |
| `Awards` | string |  |
| `BoxOffice` | string |  |
| `Country` | string |  |
| `Director` | string |  |
| `DVD` | string |  |
| `Episode` | string |  |
| `Genre` | string |  |
| `imdbID` | string |  |
| `imdbRating` | string |  |
| `imdbVotes` | string |  |
| `Language` | string |  |
| `Metascore` | string |  |
| `Plot` | string |  |
| `Poster` | string |  |
| `Production` | string |  |
| `Rated` | string |  |
| `Ratings` | array<object> |  |
| `Released` | string |  |
| `Response` | string |  |
| `Runtime` | string |  |
| `Season` | string |  |
| `seriesID` | string |  |
| `Title` | string |  |
| `totalSeasons` | string |  |
| `Type` | string |  |
| `Website` | string |  |
| `Writer` | string |  |
| `Year` | string |  |

## Native endpoint

Through the native OMDb API, this operation is `GET /` (base URL `https://www.omdbapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode-by-series-title.md) for the provider-specific parameters and requirements.


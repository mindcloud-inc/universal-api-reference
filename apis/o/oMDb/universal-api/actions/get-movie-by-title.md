# OMDb: Get Movie by Title

Retrieves movie details from OMDb by title.

```
GET https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-movie-by-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OMDb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-movie-by-title?connectionId=$CONNECTION_ID&title=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-movie-by-title?${params}`, {
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
| `title` | string | yes | Movie title to look up. |
| `year` | number | no | Release year to narrow the movie lookup. |
| `plot` | list | no | Return the short or full plot. One of: `full`, `short`. |

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

Through the native OMDb API, this operation is `GET /` (base URL `https://www.omdbapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-movie-by-title.md) for the provider-specific parameters and requirements.


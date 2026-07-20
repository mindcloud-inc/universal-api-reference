# OMDb Universal API Examples

These examples use the MindCloud API key and OMDb connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Title by IMDb ID

Retrieves title details from OMDb by IMDb ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-title-by-imdb-id?connectionId=$CONNECTION_ID&imdbId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imdbId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-title-by-imdb-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Get Title by IMDb ID action reference](actions/get-title-by-imdb-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oMDb/latest/actions/get-title-by-imdb-id).

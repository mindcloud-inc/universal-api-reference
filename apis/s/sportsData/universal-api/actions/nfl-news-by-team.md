# SportsData: NFL News By Team

Retrieves NFL news from SportsData by team.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-news-by-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-news-by-team?connectionId=$CONNECTION_ID&team=WAS" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "WAS"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-news-by-team?${params}`, {
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
| `team` | string | yes | NFL team key used by SportsData news endpoints. Example: `WAS`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "categories": "string",
      "content": "string",
      "newsID": 1,
      "originalSource": "string",
      "originalSourceUrl": "https://example.com",
      "playerID": 1,
      "playerID2": 1,
      "source": "string",
      "team": "string",
      "team2": "string",
      "teamID": 1,
      "teamID2": 1,
      "termsOfUse": "string",
      "timeAgo": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Article author. |
| `categories` | string | Article categories. |
| `content` | string | Article content excerpt. |
| `newsID` | number | SportsData news item identifier. |
| `originalSource` | string | Original publisher name. |
| `originalSourceUrl` | string | Original publisher URL. |
| `playerID` | number | Primary referenced player identifier. |
| `playerID2` | number | Secondary referenced player identifier. |
| `source` | string | Source publication for the article. |
| `team` | string | Primary referenced team abbreviation. |
| `team2` | string | Secondary referenced team abbreviation. |
| `teamID` | number | Primary referenced team identifier. |
| `teamID2` | number | Secondary referenced team identifier. |
| `termsOfUse` | string | SportsData terms-of-use text. |
| `timeAgo` | string | Human-readable recency label. |
| `title` | string | Article title. |
| `updated` | date | Last updated timestamp for the article. |
| `url` | string | Article URL. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/NewsByTeam/:team` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-news-by-team.md) for the provider-specific parameters and requirements.


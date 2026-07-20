# Botster: Run Google Search Suggestions Scraper

Creates a Botster Google search suggestions job.

```
POST https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-search-suggestions-scraper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-search-suggestions-scraper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "regionKey": "string",
  "regionLang": "string",
  "depth": "Depth 1",
  "append[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-search-suggestions-scraper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string",
    "regionKey": "string",
    "regionLang": "string",
    "depth": "Depth 1",
    "append[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Seed keywords. |
| `regionKey` | string | yes | Region. |
| `regionLang` | string | yes | Language. |
| `providers[]` | array<string> | no | Additional search engines to extract suggestions from. |
| `depth` | list | yes | Search depth. One of: `Depth 1`, `Depth 2`, `Depth 3`. |
| `append[]` | array<string> | yes | Methods for expanding the query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "bot": {
          "id": "string",
          "name": "Ava Chen"
        },
        "created_at": 1,
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.bot.id` | string | Identifier of the Botster bot that owns the job. |
| `job.bot.name` | string | Display name of the Botster bot that owns the job. |
| `job.created_at` | number | Unix timestamp when the job was created. |
| `job.id` | string | Unique Botster job identifier. |
| `job.name` | string | Botster job name. |

## Native endpoint

Through the native Botster API, this operation is `POST /bots/google-search-suggestions-scraper` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-google-search-suggestions-scraper.md) for the provider-specific parameters and requirements.


# Botster: Run Google Search Scraper

Creates a Botster Google search results extraction job.

```
POST https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-search-scraper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-search-scraper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "device": "Desktop",
  "language": "string",
  "coordinates": {},
  "os": "Android",
  "depth": "First Organic Result"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-search-scraper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string",
    "device": "Desktop",
    "language": "string",
    "coordinates": {},
    "os": "Android",
    "depth": "First Organic Result"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Search keywords and phrases. |
| `device` | list | yes | Target device type. One of: `Desktop`, `Mobile`. |
| `language` | string | yes | ISO 639-1 two-letter language code. |
| `coordinates` | object | yes | Location coordinates and zoom level for geo-specific results. |
| `os` | list | yes | Operating system for the selected device type. One of: `Android`, `Windows`, `iOS`, `macOS`. |
| `depth` | list | yes | How many search results to extract. One of: `First Organic Result`, `Top 10`, `Top 100`, `Top 20`, `Top 200`, `Top 50`, `Top 500`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cron` | string | no | Cron expression for periodic runs. |
| `newItemsOnly` | boolean | no | Return only items that appeared since the latest crawl. |

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

Through the native Botster API, this operation is `POST /bots/google-snippet-scraper` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-google-search-scraper.md) for the provider-specific parameters and requirements.


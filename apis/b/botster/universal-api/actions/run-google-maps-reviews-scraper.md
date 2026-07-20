# Botster: Run Google Maps Reviews Scraper

Creates a Botster Google review extraction job.

```
POST https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-maps-reviews-scraper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-maps-reviews-scraper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "coordinates": {},
  "depth": "string",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-maps-reviews-scraper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "coordinates": {},
    "depth": "string",
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `coordinates` | object | yes | Location coordinates and zoom level for the Google query origin. |
| `depth` | string | yes | Number of positions to inspect. |
| `input` | string | yes | Keywords, place_id, or cid. |

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

Through the native Botster API, this operation is `POST /bots/google-maps-reviews-scraper` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-google-maps-reviews-scraper.md) for the provider-specific parameters and requirements.


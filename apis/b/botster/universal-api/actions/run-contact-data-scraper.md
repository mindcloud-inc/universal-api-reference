# Botster: Run Contact Data Scraper

Creates a Botster contact data extraction job.

```
POST https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-contact-data-scraper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-contact-data-scraper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "elements[]": [
    "string"
  ],
  "input": "string",
  "limit": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-contact-data-scraper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "elements[]": ["string"],
    "input": "string",
    "limit": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `elements[]` | array<string> | yes | Contact data elements to extract. |
| `input` | string | yes | Website list. |
| `limit` | string | yes | How many pages the bot should visit. |

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

Through the native Botster API, this operation is `POST /bots/contact-data-scraper` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-contact-data-scraper.md) for the provider-specific parameters and requirements.


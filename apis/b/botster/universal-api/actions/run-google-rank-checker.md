# Botster: Run Google Rank Checker

Creates a Botster Google rank checking job.

```
POST https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-rank-checker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-rank-checker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "coordinates": {},
  "language": "string",
  "device": "Desktop",
  "os": "string",
  "domain": "example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/run-google-rank-checker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string",
    "coordinates": {},
    "language": "string",
    "device": "Desktop",
    "os": "string",
    "domain": "example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Search queries. |
| `coordinates` | object | yes | Location coordinates. |
| `language` | string | yes | Language. |
| `device` | list | yes | Device type. One of: `Desktop`, `Mobile`. |
| `os` | string | yes | Operating system. |
| `domain` | string | yes | Domain to compare. Example: `example.com`. |

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

Through the native Botster API, this operation is `POST /bots/google-rank-checker` (base URL `https://botster.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-google-rank-checker.md) for the provider-specific parameters and requirements.


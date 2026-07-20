# Cloud BOT: Run Bot

Creates a bot job in Cloud BOT.

```
POST https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/run-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/run-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicId": "string",
  "botId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/run-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicId": "string",
    "botId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicId` | string | yes |  |
| `botId` | string | yes |  |
| `timeout` | number | no | Default: `0`. |
| `callbackEndpoint` | string | no |  |
| `callbackTries` | number | no |  |
| `input` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "botName": "Ava Chen",
      "code": 1,
      "elapsedTime": 1,
      "jobId": "string",
      "output": {},
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | BOT ID |
| `botName` | string | BOT name |
| `code` | number | Response status code |
| `elapsedTime` | number | Elapsed time in seconds |
| `jobId` | string | Created job ID |
| `output` | object | BOT output object when the run finishes immediately |
| `startTime` | date | Job start time |
| `status` | number | Job status code |

## Native endpoint

Through the native Cloud BOT API, this operation is `POST /:public_id/bots/:bot_id/jobs` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-bot.md) for the provider-specific parameters and requirements.


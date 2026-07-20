# Cloud BOT: Get Bot Details

Retrieves bot details from Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/get-bot-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/get-bot-details?connectionId=$CONNECTION_ID&publicId=string&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/get-bot-details?${params}`, {
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
| `publicId` | string | yes | Public ID of API |
| `botId` | string | yes | BOT ID |
| `properties` | string | no | Comma-separated extra bot detail fields |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "description": "string",
      "icon": "string",
      "id": "string",
      "input": {},
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "output": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Response status code |
| `created` | date | BOT created date |
| `creator` | string | BOT author |
| `description` | string | BOT description |
| `icon` | string | BOT icon data URL |
| `id` | string | BOT ID |
| `input` | object | BOT input definition |
| `lastModified` | date | BOT updated date |
| `name` | string | BOT name |
| `output` | object | BOT output definition |

## Native endpoint

Through the native Cloud BOT API, this operation is `GET /:public_id/bots/:bot_id` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-details.md) for the provider-specific parameters and requirements.


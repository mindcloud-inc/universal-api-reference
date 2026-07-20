# Cloud BOT: List Bots

Retrieves bots from Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bots?connectionId=$CONNECTION_ID&publicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bots?${params}`, {
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
| `properties` | string | no | Comma-separated extra bot fields |

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
      "lastModified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
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
| `lastModified` | date | BOT updated date |
| `name` | string | BOT name |

## Native endpoint

Through the native Cloud BOT API, this operation is `GET /:public_id/bots` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bots.md) for the provider-specific parameters and requirements.


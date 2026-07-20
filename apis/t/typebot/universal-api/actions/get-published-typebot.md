# Typebot: Get Published Typebot



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-published-typebot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-published-typebot?connectionId=$CONNECTION_ID&typebotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typebotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-published-typebot?${params}`, {
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
| `typebotId` | string | yes | The Typebot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "events": [
        {
          "graphCoordinates": {
            "x": 1,
            "y": 1
          },
          "id": "string",
          "type": "string"
        }
      ],
      "id": "string",
      "lastActivityAt": "2026-05-07T12:00:00.000Z",
      "settings": {
        "general": {
          "isBrandingEnabled": true
        }
      },
      "typebotId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `events[].graphCoordinates.x` | number |  |
| `events[].graphCoordinates.y` | number |  |
| `events[].id` | string |  |
| `events[].type` | string |  |
| `id` | string |  |
| `lastActivityAt` | date |  |
| `settings.general.isBrandingEnabled` | boolean |  |
| `typebotId` | string |  |
| `updatedAt` | date |  |
| `version` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/typebots/:typebotId/publishedTypebot` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-published-typebot.md) for the provider-specific parameters and requirements.


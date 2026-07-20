# Typebot: Create Typebot



```
POST https://connect.mindcloud.co/v1/universal/typebot/latest/actions/create-typebot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/create-typebot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "typebot": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typebot/latest/actions/create-typebot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "typebot": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Workspace ID where the typebot should be created. |
| `typebot` | object | yes | Typebot object payload to create. |

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
      "isArchived": true,
      "isClosed": true,
      "name": "Ava Chen",
      "publicId": "string",
      "settings": {
        "general": {
          "isBrandingEnabled": true
        }
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": "string",
      "workspaceId": "string"
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
| `isArchived` | boolean |  |
| `isClosed` | boolean |  |
| `name` | string |  |
| `publicId` | string |  |
| `settings.general.isBrandingEnabled` | boolean |  |
| `updatedAt` | date |  |
| `version` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `POST /v1/typebots` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-typebot.md) for the provider-specific parameters and requirements.


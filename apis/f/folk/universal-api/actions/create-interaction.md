# folk: Create Interaction

Creates an interaction for a person or company in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-interaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-interaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "dateTime": "string",
  "title": "string",
  "content": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-interaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "dateTime": "string",
    "title": "string",
    "content": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes | The ID of the person or company connected to the interaction. |
| `dateTime` | string | yes | The date and time of the interaction in ISO 8601 format. |
| `title` | string | yes | The title of the interaction. |
| `content` | string | yes | The multi-line content of the interaction. |
| `type` | string | yes | An emoji or supported type token representing the interaction type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dateTime": "2026-05-07T12:00:00.000Z",
      "entity": {},
      "id": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `dateTime` | date |  |
| `entity` | object |  |
| `id` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native folk API, this operation is `POST /v1/interactions` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-interaction.md) for the provider-specific parameters and requirements.


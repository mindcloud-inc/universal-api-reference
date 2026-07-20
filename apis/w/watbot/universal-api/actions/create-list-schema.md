# Watbot: Create List Schema

Creates a new list schema in Watbot.

```
POST https://connect.mindcloud.co/v1/universal/watbot/latest/actions/create-list-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/create-list-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Stage 3 Schema",
  "fields": "[object Object]",
  "botId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/create-list-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Stage 3 Schema",
    "fields": "[object Object]",
    "botId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the list schema. Example: `Codex Stage 3 Schema`. |
| `fields` | object | yes | Field definitions for the list schema. Example: `[object Object]`. |
| `botId` | number | yes | ID of the Watbot bot that owns the list. Example: `12345`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isMenu` | boolean | no | Whether the list should appear in the Watbot menu. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": "string",
      "isMenu": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | List schema creation timestamp. |
| `fields` | object | Field definitions keyed by field slug. |
| `id` | string | List schema ID. |
| `isMenu` | boolean | Whether the list is shown in the Watbot menu. |
| `name` | string | List schema name. |
| `updatedAt` | date | List schema update timestamp. |

## Native endpoint

Through the native Watbot API, this operation is `POST /createListSchema` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-schema.md) for the provider-specific parameters and requirements.


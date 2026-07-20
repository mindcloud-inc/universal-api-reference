# LEADTEX: Create List Schema

Creates a new list schema in LEADTEX.

```
POST https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-list-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-list-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {},
  "is_menu": true,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-list-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {},
    "is_menu": true,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | object | yes | Schema fields object keyed by field slug. |
| `is_menu` | boolean | yes | Whether to show the list in the LEADTEX interface menu. |
| `name` | string | yes | List schema name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "fields": {},
        "id": "string",
        "is_menu": true,
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "errors": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.created_at` | date |  |
| `data.fields` | object |  |
| `data.id` | string |  |
| `data.is_menu` | boolean |  |
| `data.name` | string |  |
| `data.updated_at` | date |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /createListSchema?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-schema.md) for the provider-specific parameters and requirements.


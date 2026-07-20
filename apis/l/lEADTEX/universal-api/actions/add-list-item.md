# LEADTEX: Add List Item

Creates a new item in a LEADTEX list.

```
POST https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/add-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/add-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "schema_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/add-list-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "schema_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Item fields object keyed by schema field slug. |
| `schema_id` | string | yes | ID of the list schema to add the item to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contact_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
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
| `data.contact_id` | number |  |
| `data.created_at` | date |  |
| `data.id` | string |  |
| `data.updated_at` | date |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /addListItem?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-list-item.md) for the provider-specific parameters and requirements.


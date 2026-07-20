# LEADTEX: Update List Item

Updates an existing item in a LEADTEX list.

```
PUT https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/update-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/update-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "item_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/update-list-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "item_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Updated item fields object keyed by schema field slug. |
| `item_id` | string | yes | ID of the list item to update. |

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

Through the native LEADTEX API, this operation is `POST /updateListItem?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list-item.md) for the provider-specific parameters and requirements.


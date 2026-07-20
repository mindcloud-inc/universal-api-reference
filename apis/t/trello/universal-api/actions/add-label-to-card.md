# Trello: Add Label to Card

Adds a label to a Trello card.

```
PUT https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-label-to-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-label-to-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-label-to-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Card identifier. |
| `value` | string | yes | Label ID to add to the card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value[]` | string | Label ids currently attached to the card. |

## Native endpoint

Through the native Trello API, this operation is `POST cards/:id/idLabels` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-label-to-card.md) for the provider-specific parameters and requirements.


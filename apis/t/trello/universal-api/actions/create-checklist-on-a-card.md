# Trello: Create Checklist on a Card

Creates a checklist on a Trello card.

```
POST https://connect.mindcloud.co/v1/universal/trello/latest/actions/create-checklist-on-a-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trello/latest/actions/create-checklist-on-a-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trello/latest/actions/create-checklist-on-a-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Card identifier. |
| `name` | string | yes | Name for the checklist to create on card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "idBoard": "string",
      "idCard": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `idBoard` | string |  |
| `idCard` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Trello API, this operation is `POST cards/:id/checklists` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checklist-on-a-card.md) for the provider-specific parameters and requirements.


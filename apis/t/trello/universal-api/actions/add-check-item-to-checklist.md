# Trello: Add CheckItem to Checklist

Creates a check item in a Trello checklist.

```
POST https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-check-item-to-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-check-item-to-checklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-check-item-to-checklist', {
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
| `id` | string | yes | Checklist identifier. |
| `name` | string | yes | Checklist item name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "idChecklist": "string",
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `idChecklist` | string |  |
| `name` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Trello API, this operation is `POST checklists/:id/checkItems` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-check-item-to-checklist.md) for the provider-specific parameters and requirements.


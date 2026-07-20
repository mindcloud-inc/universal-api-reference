# Placker: Update Card



```
PUT https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "card": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "card": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `card` | number | yes | Card ID. Example: `12345`. |
| `title` | string | no | Updated card title. Example: `Updated task title`. |
| `description` | string | no | Updated card description. Example: `Updated task description`. |
| `status` | string | no | Updated card status. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Example: `COMPLETED`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `PATCH /card/:card` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card.md) for the provider-specific parameters and requirements.


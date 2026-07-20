# Placker: Add Card Member



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/add-card-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/add-card-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "card": "12345",
  "member.id": "987"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/add-card-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "card": "12345",
    "member.id": "987"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `card` | number | yes | Card ID. Example: `12345`. |
| `member.id` | number | yes | Member ID to add. Example: `987`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `PUT /card/:card/member` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-card-member.md) for the provider-specific parameters and requirements.


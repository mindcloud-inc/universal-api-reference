# Placker: Mirror Card To Card



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/mirror-card-to-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/mirror-card-to-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "card": "123",
  "list": "4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/mirror-card-to-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "card": "123",
    "list": "4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `card` | number | yes | Source card ID. Example: `123`. |
| `list` | number | yes | Target list ID where the mirrored card will be created. Example: `4`. |
| `position` | number | no | Optional position within the list. Example: `1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "mirror_group_id": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | ID of the created mirrored card. |
| `mirror_group_id` | string | Mirror group ID linking the source and target. |
| `status` | string | Operation status. |
| `url` | string | URL to the created card. |

## Native endpoint

Through the native Placker API, this operation is `POST /card/:card/mirror/card` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mirror-card-to-card.md) for the provider-specific parameters and requirements.


# Placker: Mirror Checklist Item To Card



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/mirror-checklist-item-to-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/mirror-checklist-item-to-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklist": "sjwa8k5le5p1c",
  "item": "sjwa8k5le5p1d",
  "list": "4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/mirror-checklist-item-to-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklist": "sjwa8k5le5p1c",
    "item": "sjwa8k5le5p1d",
    "list": "4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklist` | string | yes | Source checklist ID. Example: `sjwa8k5le5p1c`. |
| `item` | string | yes | Source checklist item ID. Example: `sjwa8k5le5p1d`. |
| `list` | number | yes | Target list ID where the card will be created. Example: `4`. |
| `title` | string | no | Optional title for the mirrored card. Example: `Mirror of item`. |
| `position` | number | no | Optional position within the list. Example: `1000`. |
| `description` | string | no | Optional description for the mirrored card. Example: `Mirrored from checklist item`. |

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

Through the native Placker API, this operation is `POST /checklist/:checklist/item/:item/mirror/card` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mirror-checklist-item-to-card.md) for the provider-specific parameters and requirements.


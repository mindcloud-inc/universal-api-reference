# InstantCard: Create Card

Creates a new draft card in InstantCard.

```
POST https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "cardTemplateId": 1,
  "cardData[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "cardTemplateId": 1,
    "cardData[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID from your InstantCard account. |
| `cardTemplateId` | number | yes | Template ID to use for the new card. |
| `cardData[]` | array<object> | yes | Array of card field objects, including text and image values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_template_id": 1,
      "data": [
        {}
      ],
      "id": 1,
      "images": [
        "string"
      ],
      "last_printed_at": "string",
      "last_submitted_at": "string",
      "organization_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_template_id` | number |  |
| `data` | array<object> |  |
| `id` | number |  |
| `images` | array<string> |  |
| `last_printed_at` | string |  |
| `last_submitted_at` | string |  |
| `organization_id` | number |  |

## Native endpoint

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/cards` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.


# InstantCard: List Cards

Retrieves all organization cards from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-cards?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-cards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from your InstantCard account. |

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
        {}
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
| `images` | array<object> |  |
| `last_printed_at` | string |  |
| `last_submitted_at` | string |  |
| `organization_id` | number |  |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/cards` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.


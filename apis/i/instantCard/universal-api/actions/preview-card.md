# InstantCard: Preview Card

Retrieves a card preview from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/preview-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/preview-card?connectionId=$CONNECTION_ID&organizationId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/preview-card?${params}`, {
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
| `id` | number | yes | ID of the card to preview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "back": "string",
      "front": "string",
      "orientation": "string",
      "preview_available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `back` | string |  |
| `front` | string |  |
| `orientation` | string |  |
| `preview_available` | boolean |  |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/cards/:id/preview` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-card.md) for the provider-specific parameters and requirements.


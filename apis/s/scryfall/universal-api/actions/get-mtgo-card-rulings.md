# Scryfall: Get MTGO Card Rulings

Retrieves card rulings from Scryfall by MTGO ID.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-mtgo-card-rulings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-mtgo-card-rulings?connectionId=$CONNECTION_ID&id=54957" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "54957"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-mtgo-card-rulings?${params}`, {
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
| `id` | number | yes | Magic Online card ID. Example: `54957`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "oracle_id": "string",
      "published_at": "2026-05-07T12:00:00.000Z",
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `oracle_id` | string |  |
| `published_at` | date |  |
| `source` | string |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET cards/mtgo/:id/rulings` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mtgo-card-rulings.md) for the provider-specific parameters and requirements.


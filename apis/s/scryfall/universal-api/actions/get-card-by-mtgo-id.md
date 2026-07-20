# Scryfall: Get Card By MTGO ID

Retrieves a card from Scryfall by MTGO ID.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-card-by-mtgo-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-card-by-mtgo-id?connectionId=$CONNECTION_ID&id=54957" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "54957"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-card-by-mtgo-id?${params}`, {
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
      "arena_id": 1,
      "collector_number": "string",
      "id": "string",
      "mtgo_id": 1,
      "multiverse_ids": [
        1
      ],
      "name": "Ava Chen",
      "object": "string",
      "oracle_text": "string",
      "scryfall_uri": "string",
      "set": "string",
      "set_name": "Ava Chen",
      "type_line": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arena_id` | number |  |
| `collector_number` | string |  |
| `id` | string |  |
| `mtgo_id` | number |  |
| `multiverse_ids` | array<number> |  |
| `name` | string |  |
| `object` | string |  |
| `oracle_text` | string |  |
| `scryfall_uri` | string |  |
| `set` | string |  |
| `set_name` | string |  |
| `type_line` | string |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET cards/mtgo/:id` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-by-mtgo-id.md) for the provider-specific parameters and requirements.


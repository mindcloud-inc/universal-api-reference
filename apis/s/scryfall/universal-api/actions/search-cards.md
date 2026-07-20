# Scryfall: Search Cards

Finds cards in Scryfall by search query.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/search-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/search-cards?connectionId=$CONNECTION_ID&q=name%3Agoblin%20type%3Acreature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "name:goblin type:creature"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/search-cards?${params}`, {
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
| `q` | string | yes | Scryfall full-text search query. Example: `name:goblin type:creature`. |
| `unique` | string | no | How duplicate prints should be collapsed, such as cards, art, or prints. |
| `order` | string | no | Sort order for matching cards, such as name, set, released, rarity, usd, eur, cmc, power, toughness, or edhrec. |
| `dir` | string | no | Sort direction, auto, asc, or desc. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeExtras` | boolean | no | Include extra cards such as tokens, planes, schemes, and funny cards. |
| `page` | number | no | Result page number for paginated card search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cmc": 1,
      "collector_number": "string",
      "id": "string",
      "layout": "string",
      "mana_cost": "string",
      "name": "Ava Chen",
      "oracle_text": "string",
      "rarity": "string",
      "released_at": "2026-05-07T12:00:00.000Z",
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
| `cmc` | number |  |
| `collector_number` | string |  |
| `id` | string |  |
| `layout` | string |  |
| `mana_cost` | string |  |
| `name` | string |  |
| `oracle_text` | string |  |
| `rarity` | string |  |
| `released_at` | date |  |
| `scryfall_uri` | string |  |
| `set` | string |  |
| `set_name` | string |  |
| `type_line` | string |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET cards/search` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cards.md) for the provider-specific parameters and requirements.


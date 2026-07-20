# Scryfall: Get Card By Name

Retrieves a card from Scryfall by name.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-card-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-card-by-name?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-card-by-name?${params}`, {
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
| `exact` | string | no |  |
| `fuzzy` | string | no |  |
| `set` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cmc": 1,
      "collector_number": "string",
      "color_identity": [
        "string"
      ],
      "colors": [
        "string"
      ],
      "highres_image": true,
      "id": "string",
      "image_status": "string",
      "lang": "string",
      "layout": "string",
      "mana_cost": "string",
      "name": "Ava Chen",
      "oracle_text": "string",
      "rarity": "string",
      "released_at": "2026-05-07T12:00:00.000Z",
      "scryfall_uri": "string",
      "set": "string",
      "set_name": "Ava Chen",
      "type_line": "string",
      "uri": "string"
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
| `color_identity` | array<string> |  |
| `colors` | array<string> |  |
| `highres_image` | boolean |  |
| `id` | string |  |
| `image_status` | string |  |
| `lang` | string |  |
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
| `uri` | string |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET cards/named` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-by-name.md) for the provider-specific parameters and requirements.


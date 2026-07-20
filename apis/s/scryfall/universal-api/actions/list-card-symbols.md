# Scryfall: List Card Symbols

Retrieves card symbols from Scryfall.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-card-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-card-symbols?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-card-symbols?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "appears_in_mana_costs": true,
      "english": "string",
      "loose_variant": "string",
      "mana_value": 1,
      "represents_mana": true,
      "symbol": "string",
      "transposable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appears_in_mana_costs` | boolean |  |
| `english` | string |  |
| `loose_variant` | string |  |
| `mana_value` | number |  |
| `represents_mana` | boolean |  |
| `symbol` | string |  |
| `transposable` | boolean |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET symbology` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-card-symbols.md) for the provider-specific parameters and requirements.


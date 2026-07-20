# Scryfall: Get Set

Retrieves a card set from Scryfall by code.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-set?connectionId=$CONNECTION_ID&code=lea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "lea"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-set?${params}`, {
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
| `code` | string | yes | Three to five-letter Scryfall or MTGO set code. Example: `lea`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_count": 1,
      "code": "string",
      "digital": true,
      "foil_only": true,
      "id": "string",
      "name": "Ava Chen",
      "nonfoil_only": true,
      "released_at": "2026-05-07T12:00:00.000Z",
      "scryfall_uri": "string",
      "set_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_count` | number |  |
| `code` | string |  |
| `digital` | boolean |  |
| `foil_only` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `nonfoil_only` | boolean |  |
| `released_at` | date |  |
| `scryfall_uri` | string |  |
| `set_type` | string |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET sets/:code` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-set.md) for the provider-specific parameters and requirements.


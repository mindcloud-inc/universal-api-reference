# Scryfall: Autocomplete Card Names

Finds card names in Scryfall by fuzzy text match.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/autocomplete-card-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/autocomplete-card-names?connectionId=$CONNECTION_ID&q=lightning" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "lightning"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/autocomplete-card-names?${params}`, {
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
| `q` | string | yes | Partial card name for autocomplete suggestions. Example: `lightning`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "object": "string",
      "total_values": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `object` | string |  |
| `total_values` | number |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET cards/autocomplete` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-card-names.md) for the provider-specific parameters and requirements.


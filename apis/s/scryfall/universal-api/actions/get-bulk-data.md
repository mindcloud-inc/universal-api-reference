# Scryfall: Get Bulk Data

Retrieves a bulk data record from Scryfall by type.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-bulk-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-bulk-data?connectionId=$CONNECTION_ID&type=oracle_cards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "oracle_cards"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/get-bulk-data?${params}`, {
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
| `type` | string | yes | Bulk data type, such as oracle_cards, unique_artwork, default_cards, all_cards, or rulings. Example: `oracle_cards`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "download_uri": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `download_uri` | string |  |
| `id` | string |  |
| `name` | string |  |
| `size` | number |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET bulk-data/:type` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-data.md) for the provider-specific parameters and requirements.


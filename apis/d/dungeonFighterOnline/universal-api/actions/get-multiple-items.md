# Dungeon Fighter Online: Get Multiple Items

Retrieves details for multiple items from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-multiple-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-multiple-items?connectionId=$CONNECTION_ID&itemIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-multiple-items?${params}`, {
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
| `itemIds` | string | yes | Comma-separated Dungeon Fighter item IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemAvailableLevel": 1,
      "itemId": "string",
      "itemName": "Ava Chen",
      "itemRarity": "string",
      "itemType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemAvailableLevel` | number |  |
| `itemId` | string |  |
| `itemName` | string |  |
| `itemRarity` | string |  |
| `itemType` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/multi/items` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-multiple-items.md) for the provider-specific parameters and requirements.


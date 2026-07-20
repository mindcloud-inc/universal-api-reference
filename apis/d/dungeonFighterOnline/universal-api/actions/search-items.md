# Dungeon Fighter Online: Search Items

Finds items in Dungeon Fighter Online by item name.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-items?connectionId=$CONNECTION_ID&itemName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-items?${params}`, {
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
| `itemName` | string | yes | Item name search term. |
| `limit` | number | no | Maximum number of items to return. Default: `5`. |

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

Through the native Dungeon Fighter Online API, this operation is `GET /df/items` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-items.md) for the provider-specific parameters and requirements.


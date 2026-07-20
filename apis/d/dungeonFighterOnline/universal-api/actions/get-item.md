# Dungeon Fighter Online: Get Item

Retrieves item details from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | Dungeon Fighter item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemAvailableLevel": 1,
      "itemExplain": "string",
      "itemId": "string",
      "itemName": "Ava Chen",
      "itemRarity": "string",
      "itemType": "string",
      "itemTypeDetail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemAvailableLevel` | number |  |
| `itemExplain` | string |  |
| `itemId` | string |  |
| `itemName` | string |  |
| `itemRarity` | string |  |
| `itemType` | string |  |
| `itemTypeDetail` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/items/:itemId` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.


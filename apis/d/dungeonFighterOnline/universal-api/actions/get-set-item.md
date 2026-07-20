# Dungeon Fighter Online: Get Set Item

Retrieves set item details from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-set-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-set-item?connectionId=$CONNECTION_ID&setItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-set-item?${params}`, {
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
| `setItemId` | string | yes | Dungeon Fighter set item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "setItemId": "string",
      "setItemName": "Ava Chen",
      "setItemOption": [
        {}
      ],
      "setItems": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `setItemId` | string |  |
| `setItemName` | string |  |
| `setItemOption` | array<object> |  |
| `setItems` | array<object> |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/setitems/:setItemId` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-set-item.md) for the provider-specific parameters and requirements.


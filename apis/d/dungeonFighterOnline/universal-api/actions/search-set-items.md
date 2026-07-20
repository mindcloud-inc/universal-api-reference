# Dungeon Fighter Online: Search Set Items

Finds set items in Dungeon Fighter Online by set name.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-set-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-set-items?connectionId=$CONNECTION_ID&setItemName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setItemName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-set-items?${params}`, {
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
| `setItemName` | string | yes | Set item name search term. |
| `limit` | number | no | Maximum number of set items to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "setItemId": "string",
      "setItemName": "Ava Chen"
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

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/setitems` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-set-items.md) for the provider-specific parameters and requirements.


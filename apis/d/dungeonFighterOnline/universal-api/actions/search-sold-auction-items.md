# Dungeon Fighter Online: Search Sold Auction Items

Finds sold auction listings in Dungeon Fighter Online by item name.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-sold-auction-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-sold-auction-items?connectionId=$CONNECTION_ID&itemName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-sold-auction-items?${params}`, {
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
| `itemName` | string | yes | Sold auction item name search term. |
| `limit` | number | no | Maximum number of sold auction records to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "itemId": "string",
      "itemName": "Ava Chen",
      "price": 1,
      "soldDate": "2026-05-07T12:00:00.000Z",
      "unitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `itemId` | string |  |
| `itemName` | string |  |
| `price` | number |  |
| `soldDate` | date |  |
| `unitPrice` | number |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/auction-sold` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sold-auction-items.md) for the provider-specific parameters and requirements.


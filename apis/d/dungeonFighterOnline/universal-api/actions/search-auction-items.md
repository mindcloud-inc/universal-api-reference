# Dungeon Fighter Online: Search Auction Items

Finds auction listings in Dungeon Fighter Online by item name.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-auction-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-auction-items?connectionId=$CONNECTION_ID&itemName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-auction-items?${params}`, {
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
| `itemName` | string | yes | Auction item name search term. |
| `limit` | number | no | Maximum number of auction listings to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auctionNo": 1,
      "count": 1,
      "currentPrice": 1,
      "expireDate": "2026-05-07T12:00:00.000Z",
      "itemId": "string",
      "itemName": "Ava Chen",
      "unitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auctionNo` | number |  |
| `count` | number |  |
| `currentPrice` | number |  |
| `expireDate` | date |  |
| `itemId` | string |  |
| `itemName` | string |  |
| `unitPrice` | number |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/auction` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-auction-items.md) for the provider-specific parameters and requirements.


# Dungeon Fighter Online: Get Auction Item

Retrieves an auction listing from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-auction-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-auction-item?connectionId=$CONNECTION_ID&auctionNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auctionNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-auction-item?${params}`, {
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
| `auctionNo` | number | yes | Auction listing number. |

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

Through the native Dungeon Fighter Online API, this operation is `GET /df/auction/:auctionNo` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auction-item.md) for the provider-specific parameters and requirements.


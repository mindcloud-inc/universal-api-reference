# Whisky Hunter: List Auctions

Retrieves online auction details from Whisky Hunter.

```
GET https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-auctions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whisky Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-auctions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/list-auctions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "base_currency": "string",
      "buyers_fee": 1,
      "listing_fee": 1,
      "name": "Ava Chen",
      "reserve_fee": 1,
      "sellers_fee": 1,
      "slug": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_currency` | string | Base currency used by the auction. |
| `buyers_fee` | number | Buyer fee percentage. |
| `listing_fee` | number | Listing fee percentage or amount. |
| `name` | string | Auction house name. |
| `reserve_fee` | number | Reserve fee percentage or amount. |
| `sellers_fee` | number | Seller fee percentage. |
| `slug` | string | Auction slug used by Whisky Hunter. |
| `url` | string | Auction house website URL. |

## Native endpoint

Through the native Whisky Hunter API, this operation is `GET /auctions_info` (base URL `https://whiskyhunter.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-auctions.md) for the provider-specific parameters and requirements.


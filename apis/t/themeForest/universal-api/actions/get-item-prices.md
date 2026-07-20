# Themeforest: Get Item Prices

Retrieves license prices for an Envato item.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-item-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-item-prices?connectionId=$CONNECTION_ID&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-item-prices?${params}`, {
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
| `itemId` | number | yes | Envato item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item_id": 1,
      "prices": [
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
| `item_id` | number | Envato item ID. |
| `prices` | array<object> | Available item prices. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/market/item-prices::item_id.json` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-prices.md) for the provider-specific parameters and requirements.


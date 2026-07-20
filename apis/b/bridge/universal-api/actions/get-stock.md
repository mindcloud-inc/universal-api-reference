# Bridge: Get Stock

Retrieves a stock from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-stock?connectionId=$CONNECTION_ID&userAccessToken=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccessToken": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-stock?${params}`, {
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
| `userAccessToken` | string | yes | Bridge user access token returned by the Authorization token action. |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "averagePurchasePrice": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "currentPrice": 1,
      "deleted": true,
      "id": 1,
      "isin": "string",
      "label": "string",
      "marketplace": "string",
      "quantity": 1,
      "stockKey": "string",
      "ticker": "string",
      "totalValue": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "valueDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Stock's linked account |
| `averagePurchasePrice` | number | Average stock purchase price |
| `createdAt` | date | Timestamp recording when the stock was created |
| `currencyCode` | string | 3 letters ISO 4217 currency code |
| `currentPrice` | number | Current unitary price for one stock |
| `deleted` | boolean | Flag to indicate that the stock was deleted |
| `id` | number | Stock's unique identifier |
| `isin` | string | Stock's ISIN [ISO 6166] (see https://en.wikipedia.org/wiki/ISO_6166) |
| `label` | string | Stock's label |
| `marketplace` | string | Marketplace where the stock is traded |
| `quantity` | number | Quantity of stocks owned |
| `stockKey` | string | Stock identification key |
| `ticker` | string | Stock 4 characters identifier |
| `totalValue` | number | Total value of this stock's portfolio = `current_price` * quantity |
| `updatedAt` | date | Timestamp recording when the stock was last refreshed |
| `valueDate` | date | The date at which the `current_price` value was recorded |

## Native endpoint

Through the native Bridge API, this operation is `GET /aggregation/stocks/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock.md) for the provider-specific parameters and requirements.


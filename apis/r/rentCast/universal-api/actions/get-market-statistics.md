# RentCast: Get Market Statistics

Retrieves market statistics from RentCast for a ZIP code.

```
GET https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-market-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RentCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-market-statistics?connectionId=$CONNECTION_ID&zipCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zipCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-market-statistics?${params}`, {
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
| `zipCode` | string | yes | A valid 5-digit US zip code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataType` | list<string> | no | The type of aggregate market data to retrieve. One of: `All`, `Rental`, `Sale`. |
| `historyRange` | number | no | The number of months of historical market data to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "rentalData": {},
      "saleData": {},
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `rentalData` | object |  |
| `saleData` | object |  |
| `zipCode` | string |  |

## Native endpoint

Through the native RentCast API, this operation is `GET /markets` (base URL `https://api.rentcast.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market-statistics.md) for the provider-specific parameters and requirements.


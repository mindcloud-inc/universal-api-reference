# ComEd: Get Latest 5-Minute Prices

Retrieves the latest 5-minute prices from ComEd.

```
GET https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get-latest5-minute-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComEd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get-latest5-minute-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get-latest5-minute-prices?${params}`, {
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
      "millisUTC": "string",
      "price": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `millisUTC` | string | UTC timestamp in milliseconds as returned by the ComEd public feed. |
| `price` | string | Price in cents per kWh as returned by the ComEd public feed. |

## Native endpoint

Through the native ComEd API, this operation is `GET /api?type=5minutefeed&format=json` (base URL `https://hourlypricing.comed.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest5-minute-prices.md) for the provider-specific parameters and requirements.


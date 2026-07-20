# WeSupply: Get Delivery Date Quotes

Retrieves delivery date quotes from WeSupply.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-delivery-date-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-delivery-date-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-delivery-date-quotes?${params}`, {
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
| `customerCountryCode` | string | no | The destination ISO country code for the quote request. |
| `customerPostalCode` | string | no | The destination postal code for the quote request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "UPS": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `UPS` | string | Carrier delivery-date quote map returned by WeSupply. |

## Native endpoint

Through the native WeSupply API, this operation is `GET /shippingQuotes` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-date-quotes.md) for the provider-specific parameters and requirements.


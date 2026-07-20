# Cloudmersive Currency: Get Exchange Rate

Retrieves an exchange rate from Cloudmersive Currency.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/get-exchange-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Currency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/get-exchange-rate?connectionId=$CONNECTION_ID&source=string&destination=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string",
  "destination": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/get-exchange-rate?${params}`, {
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
| `source` | string | yes | Source currency three-digit ISO 4217 code, such as USD or EUR. |
| `destination` | string | yes | Destination currency three-digit ISO 4217 code, such as USD or EUR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ExchangeRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ExchangeRate` | number | Exchange rate from the source currency into the destination currency. |

## Native endpoint

Through the native Cloudmersive Currency API, this operation is `POST /currency/exchange-rates/get/:source/to/:destination` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange-rate.md) for the provider-specific parameters and requirements.


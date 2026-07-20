# D7 Networks: Get SMS Pricing

Retrieves SMS pricing details from D7 Networks.

```
GET https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-pricing?${params}`, {
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
| `countryIso` | string | no | Optional ISO Alpha-2 country code, such as US or AE. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryIso": "string",
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryIso` | string | Country ISO code. |
| `price` | number | SMS price for the country. |

## Native endpoint

Through the native D7 Networks API, this operation is `GET /messages/v1/sms/pricing` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-pricing.md) for the provider-specific parameters and requirements.


# Byteplant Address Validator: Get Address Details

Retrieves address details from Byteplant Address Validator by suggestion ID.

```
GET https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/get-address-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Byteplant Address Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/get-address-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/get-address-details?${params}`, {
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
| `id` | string | yes | Address id returned by Search Address Suggestions. |
| `geocoding` | boolean | no | Include latitude and longitude in the response. Default: `false`. |
| `timeout` | number | no | Request timeout in seconds. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "cost": 1,
      "country": "string",
      "county": "string",
      "formattedaddress": "string",
      "postalcode": "string",
      "ratelimit_remain": 1,
      "ratelimit_seconds": 1,
      "state": "string",
      "status": "string",
      "street": "string",
      "streetnumber": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Normalized city. |
| `cost` | number | Credits consumed by the request. |
| `country` | string | Normalized ISO country code. |
| `county` | string | County or regional subdivision. |
| `formattedaddress` | string | Normalized full address. |
| `postalcode` | string | Normalized postal code. |
| `ratelimit_remain` | number | Remaining requests in the current rate-limit window. |
| `ratelimit_seconds` | number | Seconds remaining in the current rate-limit window. |
| `state` | string | Normalized state or province. |
| `status` | string | Byteplant retrieval status. |
| `street` | string | Normalized street name. |
| `streetnumber` | string | Normalized street number. |
| `type` | string | Address type code. |

## Native endpoint

Through the native Byteplant Address Validator API, this operation is `GET /api/fetch` (base URL `https://api.address-validator.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-details.md) for the provider-specific parameters and requirements.


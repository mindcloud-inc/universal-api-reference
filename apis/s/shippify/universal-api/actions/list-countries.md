# Shippify: List Countries

Retrieves the list of supported countries from Shippify.

```
GET https://connect.mindcloud.co/v1/universal/shippify/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/list-countries?${params}`, {
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
      "countryCode": "string",
      "createdAt": "string",
      "defaultCityId": 1,
      "defaultCityName": "Ava Chen",
      "id": 1,
      "isSaasVisible": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | string | ISO-style Shippify country code. |
| `createdAt` | string | Country creation timestamp. |
| `defaultCityId` | number | Default city identifier for the country when available. |
| `defaultCityName` | string | Default city name for the country when available. |
| `id` | number | Country identifier. |
| `isSaasVisible` | number | Whether the country is visible in Shippify's SaaS experience. |
| `name` | string | Country name. |

## Native endpoint

Through the native Shippify API, this operation is `GET /v1/country` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.


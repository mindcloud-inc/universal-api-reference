# Seven: Get Pricing

Retrieves pricing information from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-pricing?connectionId=$CONNECTION_ID&country=string&format=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "format": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-pricing?${params}`, {
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
| `country` | string | yes | Country Code according to ISO-3166 (ALPHA-2) for which you want to query the prices. If this parameter is not specified, the prices of all countries are displayed. |
| `format` | string | yes | By default, the data is returned as JSON. However, you can also request a CSV format. To do this, use the parameter format=csv |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countCountries": 1,
      "countNetworks": 1,
      "countries": {
        "countryCode": "string",
        "countryName": "Ava Chen",
        "countryPrefix": "string",
        "networks": {
          "comment": "string",
          "features": [
            "string"
          ],
          "mcc": "string",
          "mncs": [
            "string"
          ],
          "networkName": "Ava Chen",
          "price": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countCountries` | number |  |
| `countNetworks` | number |  |
| `countries` | array<object> |  |
| `countries.countryCode` | string |  |
| `countries.countryName` | string |  |
| `countries.countryPrefix` | string |  |
| `countries.networks` | array<object> |  |
| `countries.networks.comment` | string |  |
| `countries.networks.features` | array<string> |  |
| `countries.networks.mcc` | string |  |
| `countries.networks.mncs` | array<string> |  |
| `countries.networks.networkName` | string |  |
| `countries.networks.price` | number |  |

## Native endpoint

Through the native Seven API, this operation is `GET /pricing` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing.md) for the provider-specific parameters and requirements.


# REST Countries: Get Country Currencies by Code



```
GET https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/get-country-currencies-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a REST Countries `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/get-country-currencies-by-code?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/get-country-currencies-by-code?${params}`, {
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
| `code` | string | yes | ISO 3166-1 alpha-2 or alpha-3 country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencies": {},
      "name": {
        "common": "Ava Chen",
        "official": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencies` | object |  |
| `name.common` | string |  |
| `name.official` | string |  |

## Native endpoint

Through the native REST Countries API, this operation is `GET alpha/:code?fields=name,currencies` (base URL `https://restcountries.com/v3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-currencies-by-code.md) for the provider-specific parameters and requirements.


# AccuWeather: Search Postal Codes

Finds locations in AccuWeather by postal code.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-postal-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-postal-codes?connectionId=$CONNECTION_ID&q=10021" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "10021"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/search-postal-codes?${params}`, {
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
| `q` | string | yes | Required postal code text. Default: `10021`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Key": "string",
      "LocalizedName": "Ava Chen",
      "PrimaryPostalCode": "string",
      "Version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Key` | string |  |
| `LocalizedName` | string |  |
| `PrimaryPostalCode` | string |  |
| `Version` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /locations/v1/postalcodes/search` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-postal-codes.md) for the provider-specific parameters and requirements.


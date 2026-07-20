# Cloudmersive: List ISO 3166-1 Countries

Retrieves ISO 3166-1 countries from Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/list-iso31661-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/list-iso31661-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/list-iso31661-countries?${params}`, {
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
      "countries": [
        {
          "countryName": "Ava Chen",
          "currencyEnglishName": "Ava Chen",
          "isoCurrencyCode": "string",
          "isoTwoLetterCode": "string",
          "region": "string",
          "subregion": "string",
          "threeLetterCode": "string"
        }
      ],
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries` | array<object> |  |
| `countries[].countryName` | string |  |
| `countries[].currencyEnglishName` | string |  |
| `countries[].isoCurrencyCode` | string |  |
| `countries[].isoTwoLetterCode` | string |  |
| `countries[].region` | string |  |
| `countries[].subregion` | string |  |
| `countries[].threeLetterCode` | string |  |
| `successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/country/list` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-iso31661-countries.md) for the provider-specific parameters and requirements.


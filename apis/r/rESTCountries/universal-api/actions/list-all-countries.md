# REST Countries: List All Countries



```
GET https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-all-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a REST Countries `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-all-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-all-countries?${params}`, {
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
      "capital": [
        "string"
      ],
      "cca2": "string",
      "cca3": "string",
      "flags": {
        "alt": "string",
        "png": "string",
        "svg": "string"
      },
      "independent": true,
      "name": {
        "common": "Ava Chen",
        "official": "Ava Chen"
      },
      "population": 1,
      "region": "string",
      "subregion": "string",
      "unMember": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capital` | array<string> |  |
| `cca2` | string |  |
| `cca3` | string |  |
| `flags.alt` | string |  |
| `flags.png` | string |  |
| `flags.svg` | string |  |
| `independent` | boolean |  |
| `name.common` | string |  |
| `name.official` | string |  |
| `population` | number |  |
| `region` | string |  |
| `subregion` | string |  |
| `unMember` | boolean |  |

## Native endpoint

Through the native REST Countries API, this operation is `GET all?fields=name,cca2,cca3,region,subregion,capital,population,independent,unMember,flags` (base URL `https://restcountries.com/v3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-countries.md) for the provider-specific parameters and requirements.


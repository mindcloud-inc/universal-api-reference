# REST Countries: List Country Names and Flags



```
GET https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-names-and-flags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a REST Countries `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-names-and-flags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-names-and-flags?${params}`, {
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
      "cca2": "string",
      "cca3": "string",
      "flags": {
        "alt": "string",
        "png": "string",
        "svg": "string"
      },
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
| `cca2` | string |  |
| `cca3` | string |  |
| `flags.alt` | string |  |
| `flags.png` | string |  |
| `flags.svg` | string |  |
| `name.common` | string |  |
| `name.official` | string |  |

## Native endpoint

Through the native REST Countries API, this operation is `GET all?fields=name,flags,cca2,cca3` (base URL `https://restcountries.com/v3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-country-names-and-flags.md) for the provider-specific parameters and requirements.


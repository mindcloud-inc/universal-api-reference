# Print.one Postcards: List Supported Countries

Retrieves supported countries from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-supported-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-supported-countries?${params}`, {
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
      "alternativeNames": [
        "Ava Chen"
      ],
      "englishName": "Ava Chen",
      "internationalDuration": "string",
      "iso31661Alpha2": "string",
      "iso31661Alpha3": "string",
      "nativeName": "Ava Chen",
      "phonePrefix": "string",
      "region": "string",
      "supported": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternativeNames[]` | string |  |
| `englishName` | string |  |
| `internationalDuration` | string |  |
| `iso31661Alpha2` | string |  |
| `iso31661Alpha3` | string |  |
| `nativeName` | string |  |
| `phonePrefix` | string |  |
| `region` | string |  |
| `supported` | boolean |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/countries` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-countries.md) for the provider-specific parameters and requirements.


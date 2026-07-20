# Hopewiser: List International Countries



```
GET https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/list-international-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hopewiser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/list-international-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/list-international-countries?${params}`, {
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
      "code2": "string",
      "code3": "string",
      "coverageLevel": "string",
      "customPickList": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code2` | string | ISO 3166-1 alpha-2 country code. |
| `code3` | string | ISO 3166-1 alpha-3 country code. |
| `coverageLevel` | string | Hopewiser international coverage level. |
| `customPickList` | boolean | Whether the country uses a custom pick-list. |
| `name` | string | Country name. |

## Native endpoint

Through the native Hopewiser API, this operation is `GET /atlaslive/countries/json` (base URL `https://cloud.hopewiser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-international-countries.md) for the provider-specific parameters and requirements.


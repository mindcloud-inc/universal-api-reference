# REST Countries: List Country Start of Week



```
GET https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-start-of-week
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a REST Countries `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-start-of-week?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-start-of-week?${params}`, {
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
      "name": {
        "common": "Ava Chen",
        "official": "Ava Chen"
      },
      "startOfWeek": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name.common` | string |  |
| `name.official` | string |  |
| `startOfWeek` | string |  |

## Native endpoint

Through the native REST Countries API, this operation is `GET all?fields=name,startOfWeek` (base URL `https://restcountries.com/v3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-country-start-of-week.md) for the provider-specific parameters and requirements.


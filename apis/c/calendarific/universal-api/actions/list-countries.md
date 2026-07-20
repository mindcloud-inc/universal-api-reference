# Calendarific: List Countries

Retrieves supported countries from Calendarific.

```
GET https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendarific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-countries?${params}`, {
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
      "countryName": "Ava Chen",
      "flagUnicode": "string",
      "iso3166": "string",
      "supportedLanguages": 1,
      "totalHolidays": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryName` | string | Country name. |
| `flagUnicode` | string | Unicode flag for the country. |
| `iso3166` | string | ISO 3166 country code. |
| `supportedLanguages` | number | Number of supported languages for the country. |
| `totalHolidays` | number | Number of holidays supported for the country. |
| `uuid` | string | Calendarific country identifier. |

## Native endpoint

Through the native Calendarific API, this operation is `GET /countries` (base URL `https://calendarific.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.


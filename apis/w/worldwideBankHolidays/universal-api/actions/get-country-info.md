# Worldwide Bank Holidays: Get Country Info



```
GET https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/get-country-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worldwide Bank Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/get-country-info?connectionId=$CONNECTION_ID&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/get-country-info?${params}`, {
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
| `countryCode` | string | yes | ISO 3166-1 alpha-2 country code, such as US or DE. Default: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "borders": [
        {}
      ],
      "commonName": "Ava Chen",
      "countryCode": "string",
      "officialName": "Ava Chen",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `borders` | array<object> | Neighboring countries. |
| `commonName` | string | Common country name. |
| `countryCode` | string | ISO 3166-1 alpha-2 country code. |
| `officialName` | string | Official country name. |
| `region` | string | Geopolitical or continental region. |

## Native endpoint

Through the native Worldwide Bank Holidays API, this operation is `GET /api/v3/CountryInfo/{{countryCode}}` (base URL `https://date.nager.at`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-info.md) for the provider-specific parameters and requirements.


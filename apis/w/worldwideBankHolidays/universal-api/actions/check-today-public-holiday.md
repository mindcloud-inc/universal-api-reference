# Worldwide Bank Holidays: Check Today Public Holiday



```
GET https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/check-today-public-holiday
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worldwide Bank Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/check-today-public-holiday?connectionId=$CONNECTION_ID&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/check-today-public-holiday?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countyCode` | string | no | Optional subdivision/county code. |
| `offset` | number | no | Optional UTC timezone offset from -12 to 12. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | HTTP status indicator: 200 means today is a public holiday, 204 means it is not, and 404 means the country was not found. |

## Native endpoint

Through the native Worldwide Bank Holidays API, this operation is `GET /api/v3/IsTodayPublicHoliday/{{countryCode}}` (base URL `https://date.nager.at`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-today-public-holiday.md) for the provider-specific parameters and requirements.


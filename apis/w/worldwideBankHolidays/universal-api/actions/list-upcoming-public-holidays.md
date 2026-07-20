# Worldwide Bank Holidays: List Upcoming Public Holidays



```
GET https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/list-upcoming-public-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worldwide Bank Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/list-upcoming-public-holidays?connectionId=$CONNECTION_ID&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/list-upcoming-public-holidays?${params}`, {
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
      "counties": [
        "string"
      ],
      "countryCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "fixed": true,
      "global": true,
      "launchYear": 1,
      "localName": "Ava Chen",
      "name": "Ava Chen",
      "types": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `counties` | array<string> | ISO 3166-2 subdivision codes where applicable. |
| `countryCode` | string | ISO 3166-1 alpha-2 country code. |
| `date` | date | Holiday date. |
| `fixed` | boolean | Whether the holiday occurs on the same date each year. |
| `global` | boolean | Whether the holiday applies to the entire country. |
| `launchYear` | number | Year the holiday was first observed. |
| `localName` | string | Local name of the holiday. |
| `name` | string | English holiday name. |
| `types` | array<string> | Holiday type values. |

## Native endpoint

Through the native Worldwide Bank Holidays API, this operation is `GET /api/v3/NextPublicHolidays/{{countryCode}}` (base URL `https://date.nager.at`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-upcoming-public-holidays.md) for the provider-specific parameters and requirements.


# Worldwide Bank Holidays: List Long Weekends



```
GET https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/list-long-weekends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worldwide Bank Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/list-long-weekends?connectionId=$CONNECTION_ID&year=2026&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026",
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/list-long-weekends?${params}`, {
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
| `year` | number | yes | Calendar year for long weekend lookup. Default: `2026`. |
| `countryCode` | string | yes | ISO 3166-1 alpha-2 country code, such as US or DE. Default: `US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `availableBridgeDays` | number | no | Optional number of available bridge days, from 1 to 100. Default: `1`. |
| `subdivisionCode` | string | no | Optional ISO 3166-2 subdivision code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bridgeDays": [
        "2026-05-07T12:00:00.000Z"
      ],
      "dayCount": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "needBridgeDay": true,
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bridgeDays` | array<date> | Optional bridge days that extend the weekend. |
| `dayCount` | number | Total days in the long weekend. |
| `endDate` | date | End date of the long weekend. |
| `needBridgeDay` | boolean | Whether a bridge day is required. |
| `startDate` | date | Start date of the long weekend. |

## Native endpoint

Through the native Worldwide Bank Holidays API, this operation is `GET /api/v3/LongWeekend/{{year}}/{{countryCode}}` (base URL `https://date.nager.at`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-long-weekends.md) for the provider-specific parameters and requirements.


# Cloudmersive: Get Public Holidays

Retrieves public holidays by country and year in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-public-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-public-holidays?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-public-holidays?${params}`, {
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
| `RawCountryInput` | string | no | Two-letter country code for the holiday lookup. |
| `Year` | string | no | Optional year for the holiday lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "publicHolidays": [
        {
          "englishName": "Ava Chen",
          "holidayType": "string",
          "localName": "Ava Chen",
          "nationwide": true,
          "occurrenceDate": "2026-05-07T12:00:00.000Z"
        }
      ],
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publicHolidays` | array<object> |  |
| `publicHolidays[].englishName` | string |  |
| `publicHolidays[].holidayType` | string |  |
| `publicHolidays[].localName` | string |  |
| `publicHolidays[].nationwide` | boolean |  |
| `publicHolidays[].occurrenceDate` | date |  |
| `successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/date-time/get/holidays` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-holidays.md) for the provider-specific parameters and requirements.


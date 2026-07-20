# Hebcal: Get Shabbat Times for Date

Retrieves Shabbat times for a date from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-shabbat-times-for-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-shabbat-times-for-date?connectionId=$CONNECTION_ID&gy=string&gm=string&gd=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gy": "string",
  "gm": "string",
  "gd": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-shabbat-times-for-date?${params}`, {
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
| `gy` | string | yes | Gregorian year. |
| `gm` | string | yes | Gregorian month number. |
| `gd` | string | yes | Gregorian day of month. |
| `lg` | string | no | Event title language. |
| `b` | string | no | Minutes before sunset for candle lighting. |
| `m` | string | no | Fixed minutes after sundown for havdalah. |
| `geonameid` | string | no | GeoNames numeric ID for the location. |
| `zip` | string | no | United States ZIP code for the location. |
| `latitude` | string | no | Latitude for the location. |
| `longitude` | string | no | Longitude for the location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "items": [
        [
          {}
        ]
      ],
      "location": {
        "admin1": "string",
        "asciiname": "Ava Chen",
        "cc": "string",
        "city": "string",
        "country": "string",
        "elevation": 1,
        "geo": "string",
        "geonameid": 1,
        "latitude": 1,
        "longitude": 1,
        "title": "string",
        "tzid": "string"
      },
      "range": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `items[]` | array<object> |  |
| `items[].category` | string |  |
| `items[].date` | date |  |
| `items[].hdate` | string |  |
| `items[].hebrew` | string |  |
| `items[].link` | string |  |
| `items[].memo` | string |  |
| `items[].subcat` | string |  |
| `items[].title` | string |  |
| `location.admin1` | string |  |
| `location.asciiname` | string |  |
| `location.cc` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.elevation` | number |  |
| `location.geo` | string |  |
| `location.geonameid` | number |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.title` | string |  |
| `location.tzid` | string |  |
| `range.end` | date |  |
| `range.start` | date |  |
| `title` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /shabbat` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shabbat-times-for-date.md) for the provider-specific parameters and requirements.


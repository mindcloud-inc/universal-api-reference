# Hebcal: List Yizkor Dates

Retrieves Yizkor dates from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/list-yizkor-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/list-yizkor-dates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/list-yizkor-dates?${params}`, {
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
| `year` | string | no | Gregorian year or now. |
| `month` | string | no | Gregorian month number or x for whole year. |
| `start` | string | no | Gregorian start date in YYYY-MM-DD format. |
| `end` | string | no | Gregorian end date in YYYY-MM-DD format. |
| `lg` | string | no | Event title language. |
| `i` | string | no | Use Israel holiday schedule when enabled. |
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
| `items[].hebrew` | string |  |
| `items[].title` | string |  |
| `items[].title_orig` | string |  |
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

Through the native Hebcal API, this operation is `GET /hebcal` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-yizkor-dates.md) for the provider-specific parameters and requirements.


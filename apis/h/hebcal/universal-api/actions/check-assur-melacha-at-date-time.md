# Hebcal: Check Assur Melacha at Date Time

Checks whether work is forbidden at a date and time in Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/check-assur-melacha-at-date-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/check-assur-melacha-at-date-time?connectionId=$CONNECTION_ID&dt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/check-assur-melacha-at-date-time?${params}`, {
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
| `dt` | string | yes | ISO 8601 date-time to check. |
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
      "location": {
        "admin1": "string",
        "asciiname": "Ava Chen",
        "cc": "string",
        "city": "string",
        "country": "string",
        "geo": "string",
        "geonameid": 1,
        "latitude": 1,
        "longitude": 1,
        "title": "string",
        "tzid": "string"
      },
      "status": {
        "isAssurBemlacha": true,
        "localTime": "2026-05-07T12:00:00.000Z"
      },
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
| `location.admin1` | string |  |
| `location.asciiname` | string |  |
| `location.cc` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.geo` | string |  |
| `location.geonameid` | number |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.title` | string |  |
| `location.tzid` | string |  |
| `status.isAssurBemlacha` | boolean |  |
| `status.localTime` | date |  |
| `version` | string |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /zmanim` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-assur-melacha-at-date-time.md) for the provider-specific parameters and requirements.


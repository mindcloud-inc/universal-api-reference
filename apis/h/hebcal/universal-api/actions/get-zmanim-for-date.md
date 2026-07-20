# Hebcal: Get Zmanim for Date

Retrieves zmanim for a date from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-zmanim-for-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-zmanim-for-date?connectionId=$CONNECTION_ID&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-zmanim-for-date?${params}`, {
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
| `date` | string | yes | Gregorian date in YYYY-MM-DD format. |
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
      "times": {
        "alosBaalHatanya": "2026-05-07T12:00:00.000Z",
        "alotHaShachar": "2026-05-07T12:00:00.000Z",
        "beinHaShmashos": "2026-05-07T12:00:00.000Z",
        "chatzot": "2026-05-07T12:00:00.000Z",
        "chatzotNight": "2026-05-07T12:00:00.000Z",
        "dawn": "2026-05-07T12:00:00.000Z",
        "dusk": "2026-05-07T12:00:00.000Z",
        "minchaGedola": "2026-05-07T12:00:00.000Z",
        "minchaGedolaBaalHatanya": "2026-05-07T12:00:00.000Z",
        "minchaGedolaMGA": "2026-05-07T12:00:00.000Z",
        "minchaKetana": "2026-05-07T12:00:00.000Z",
        "minchaKetanaBaalHatanya": "2026-05-07T12:00:00.000Z",
        "minchaKetanaMGA": "2026-05-07T12:00:00.000Z",
        "misheyakir": "2026-05-07T12:00:00.000Z",
        "misheyakirMachmir": "2026-05-07T12:00:00.000Z",
        "plagHaMincha": "2026-05-07T12:00:00.000Z",
        "plagHaminchaBaalHatanya": "2026-05-07T12:00:00.000Z",
        "sofZmanShma": "2026-05-07T12:00:00.000Z",
        "sofZmanShmaBaalHatanya": "2026-05-07T12:00:00.000Z",
        "sofZmanShmaMGA": "2026-05-07T12:00:00.000Z",
        "sofZmanShmaMGA16Point1": "2026-05-07T12:00:00.000Z",
        "sofZmanShmaMGA19Point8": "2026-05-07T12:00:00.000Z",
        "sofZmanTfilaBaalHatanya": "2026-05-07T12:00:00.000Z",
        "sofZmanTfilla": "2026-05-07T12:00:00.000Z",
        "sofZmanTfillaMGA": "2026-05-07T12:00:00.000Z",
        "sofZmanTfillaMGA16Point1": "2026-05-07T12:00:00.000Z",
        "sofZmanTfillaMGA19Point8": "2026-05-07T12:00:00.000Z",
        "sunrise": "2026-05-07T12:00:00.000Z",
        "sunset": "2026-05-07T12:00:00.000Z",
        "tzaisBaalHatanya": "2026-05-07T12:00:00.000Z",
        "tzeit42min": "2026-05-07T12:00:00.000Z",
        "tzeit50min": "2026-05-07T12:00:00.000Z",
        "tzeit7083deg": "2026-05-07T12:00:00.000Z",
        "tzeit72min": "2026-05-07T12:00:00.000Z",
        "tzeit85deg": "2026-05-07T12:00:00.000Z"
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
| `times.alosBaalHatanya` | date |  |
| `times.alotHaShachar` | date |  |
| `times.beinHaShmashos` | date |  |
| `times.chatzot` | date |  |
| `times.chatzotNight` | date |  |
| `times.dawn` | date |  |
| `times.dusk` | date |  |
| `times.minchaGedola` | date |  |
| `times.minchaGedolaBaalHatanya` | date |  |
| `times.minchaGedolaMGA` | date |  |
| `times.minchaKetana` | date |  |
| `times.minchaKetanaBaalHatanya` | date |  |
| `times.minchaKetanaMGA` | date |  |
| `times.misheyakir` | date |  |
| `times.misheyakirMachmir` | date |  |
| `times.plagHaMincha` | date |  |
| `times.plagHaminchaBaalHatanya` | date |  |
| `times.sofZmanShma` | date |  |
| `times.sofZmanShmaBaalHatanya` | date |  |
| `times.sofZmanShmaMGA` | date |  |
| `times.sofZmanShmaMGA16Point1` | date |  |
| `times.sofZmanShmaMGA19Point8` | date |  |
| `times.sofZmanTfilaBaalHatanya` | date |  |
| `times.sofZmanTfilla` | date |  |
| `times.sofZmanTfillaMGA` | date |  |
| `times.sofZmanTfillaMGA16Point1` | date |  |
| `times.sofZmanTfillaMGA19Point8` | date |  |
| `times.sunrise` | date |  |
| `times.sunset` | date |  |
| `times.tzaisBaalHatanya` | date |  |
| `times.tzeit42min` | date |  |
| `times.tzeit50min` | date |  |
| `times.tzeit7083deg` | date |  |
| `times.tzeit72min` | date |  |
| `times.tzeit85deg` | date |  |
| `version` | string |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /zmanim` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zmanim-for-date.md) for the provider-specific parameters and requirements.


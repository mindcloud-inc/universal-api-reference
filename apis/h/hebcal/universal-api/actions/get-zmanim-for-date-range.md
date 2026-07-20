# Hebcal: Get Zmanim for Date Range

Retrieves zmanim for a date range from Hebcal.

```
GET https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-zmanim-for-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hebcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-zmanim-for-date-range?connectionId=$CONNECTION_ID&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hebcal/latest/actions/get-zmanim-for-date-range?${params}`, {
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
| `start` | string | yes | Gregorian start date in YYYY-MM-DD format. |
| `end` | string | yes | Gregorian end date in YYYY-MM-DD format. |
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
      "date": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
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
        "alosBaalHatanya": [
          [
            {}
          ]
        ],
        "alotHaShachar": [
          [
            {}
          ]
        ],
        "beinHaShmashos": [
          [
            {}
          ]
        ],
        "chatzot": [
          [
            {}
          ]
        ],
        "chatzotNight": [
          [
            {}
          ]
        ],
        "dawn": [
          [
            {}
          ]
        ],
        "dusk": [
          [
            {}
          ]
        ],
        "minchaGedola": [
          [
            {}
          ]
        ],
        "minchaGedolaBaalHatanya": [
          [
            {}
          ]
        ],
        "minchaGedolaMGA": [
          [
            {}
          ]
        ],
        "minchaKetana": [
          [
            {}
          ]
        ],
        "minchaKetanaBaalHatanya": [
          [
            {}
          ]
        ],
        "minchaKetanaMGA": [
          [
            {}
          ]
        ],
        "misheyakir": [
          [
            {}
          ]
        ],
        "misheyakirMachmir": [
          [
            {}
          ]
        ],
        "plagHaMincha": [
          [
            {}
          ]
        ],
        "plagHaminchaBaalHatanya": [
          [
            {}
          ]
        ],
        "sofZmanShma": [
          [
            {}
          ]
        ],
        "sofZmanShmaBaalHatanya": [
          [
            {}
          ]
        ],
        "sofZmanShmaMGA": [
          [
            {}
          ]
        ],
        "sofZmanShmaMGA16Point1": [
          [
            {}
          ]
        ],
        "sofZmanShmaMGA19Point8": [
          [
            {}
          ]
        ],
        "sofZmanTfilaBaalHatanya": [
          [
            {}
          ]
        ],
        "sofZmanTfilla": [
          [
            {}
          ]
        ],
        "sofZmanTfillaMGA": [
          [
            {}
          ]
        ],
        "sofZmanTfillaMGA16Point1": [
          [
            {}
          ]
        ],
        "sofZmanTfillaMGA19Point8": [
          [
            {}
          ]
        ],
        "sunrise": [
          [
            {}
          ]
        ],
        "sunset": [
          [
            {}
          ]
        ],
        "tzaisBaalHatanya": [
          [
            {}
          ]
        ],
        "tzeit42min": [
          [
            {}
          ]
        ],
        "tzeit50min": [
          [
            {}
          ]
        ],
        "tzeit7083deg": [
          [
            {}
          ]
        ],
        "tzeit72min": [
          [
            {}
          ]
        ],
        "tzeit85deg": [
          [
            {}
          ]
        ]
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
| `date.end` | date |  |
| `date.start` | date |  |
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
| `times.alosBaalHatanya[]` | array<object> |  |
| `times.alotHaShachar[]` | array<object> |  |
| `times.beinHaShmashos[]` | array<object> |  |
| `times.chatzot[]` | array<object> |  |
| `times.chatzotNight[]` | array<object> |  |
| `times.dawn[]` | array<object> |  |
| `times.dusk[]` | array<object> |  |
| `times.minchaGedola[]` | array<object> |  |
| `times.minchaGedolaBaalHatanya[]` | array<object> |  |
| `times.minchaGedolaMGA[]` | array<object> |  |
| `times.minchaKetana[]` | array<object> |  |
| `times.minchaKetanaBaalHatanya[]` | array<object> |  |
| `times.minchaKetanaMGA[]` | array<object> |  |
| `times.misheyakir[]` | array<object> |  |
| `times.misheyakirMachmir[]` | array<object> |  |
| `times.plagHaMincha[]` | array<object> |  |
| `times.plagHaminchaBaalHatanya[]` | array<object> |  |
| `times.sofZmanShma[]` | array<object> |  |
| `times.sofZmanShmaBaalHatanya[]` | array<object> |  |
| `times.sofZmanShmaMGA[]` | array<object> |  |
| `times.sofZmanShmaMGA16Point1[]` | array<object> |  |
| `times.sofZmanShmaMGA19Point8[]` | array<object> |  |
| `times.sofZmanTfilaBaalHatanya[]` | array<object> |  |
| `times.sofZmanTfilla[]` | array<object> |  |
| `times.sofZmanTfillaMGA[]` | array<object> |  |
| `times.sofZmanTfillaMGA16Point1[]` | array<object> |  |
| `times.sofZmanTfillaMGA19Point8[]` | array<object> |  |
| `times.sunrise[]` | array<object> |  |
| `times.sunset[]` | array<object> |  |
| `times.tzaisBaalHatanya[]` | array<object> |  |
| `times.tzeit42min[]` | array<object> |  |
| `times.tzeit50min[]` | array<object> |  |
| `times.tzeit7083deg[]` | array<object> |  |
| `times.tzeit72min[]` | array<object> |  |
| `times.tzeit85deg[]` | array<object> |  |
| `version` | string |  |

## Native endpoint

Through the native Hebcal API, this operation is `GET /zmanim` (base URL `https://www.hebcal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zmanim-for-date-range.md) for the provider-specific parameters and requirements.


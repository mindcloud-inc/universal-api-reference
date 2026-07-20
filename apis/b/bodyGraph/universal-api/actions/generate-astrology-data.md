# BodyGraph: Generate Astrology Data

Retrieves astrology chart data from BodyGraph.

```
GET https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/generate-astrology-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BodyGraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/generate-astrology-data?connectionId=$CONNECTION_ID&date=2019-05-05%2010%3A10&timezone=Europe%2FLondon&latitude=51.509865&longitude=-0.118092&houseSystem=W" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2019-05-05 10:10",
  "timezone": "Europe/London",
  "latitude": "51.509865",
  "longitude": "-0.118092",
  "houseSystem": "W"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/generate-astrology-data?${params}`, {
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
| `date` | string | yes | Local date of birth. Format: Y-M-D H:I Example: `2019-05-05 10:10`. |
| `timezone` | string | yes | Timezone of place of birth. Example: `Europe/London`. |
| `latitude` | string | yes | Latitude of place of birth. Example: `51.509865`. |
| `longitude` | string | yes | Longitude of place of birth. Example: `-0.118092`. |
| `houseSystem` | string | yes | House system code, for example W for whole sign or P for Placidus. Example: `W`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `design` | string | no | Exact chart design title from your Chart Designs dashboard. Adds SVG output when provided. Example: `My Default Design`. |
| `language` | string | no | Exact language title from your Chart Content tool for localized output. Example: `English`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ASCMC": [
        1
      ],
      "Aspects": {},
      "Houses": [
        {}
      ],
      "Planets": {},
      "Properties": {},
      "Zodiacs": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ASCMC` | array<number> |  |
| `Aspects` | object |  |
| `Houses` | array<object> |  |
| `Planets` | object |  |
| `Properties` | object |  |
| `Zodiacs` | object |  |

## Native endpoint

Through the native BodyGraph API, this operation is `GET /v240815/astro-data` (base URL `https://api.bodygraphchart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-astrology-data.md) for the provider-specific parameters and requirements.


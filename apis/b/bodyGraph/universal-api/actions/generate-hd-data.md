# BodyGraph: Generate HD Data

Retrieves Human Design chart data from BodyGraph.

```
GET https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/generate-hd-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BodyGraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/generate-hd-data?connectionId=$CONNECTION_ID&date=2019-05-05%2010%3A10&timezone=Europe%2FLondon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2019-05-05 10:10",
  "timezone": "Europe/London"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/generate-hd-data?${params}`, {
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
      "Channels": [
        "string"
      ],
      "ChartUrl": "https://example.com",
      "ConsciousCenters": [
        "string"
      ],
      "DefinedCenters": [
        "string"
      ],
      "Design": {},
      "Gates": [
        1
      ],
      "OpenCenters": [
        "string"
      ],
      "Personality": {},
      "Planets": [
        {}
      ],
      "Properties": {},
      "UnconsciousCenters": [
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
| `Channels` | array<string> |  |
| `ChartUrl` | string |  |
| `ConsciousCenters` | array<string> |  |
| `DefinedCenters` | array<string> |  |
| `Design` | object |  |
| `Gates` | array<number> |  |
| `OpenCenters` | array<string> |  |
| `Personality` | object |  |
| `Planets` | array<object> |  |
| `Properties` | object |  |
| `UnconsciousCenters` | array<string> |  |

## Native endpoint

Through the native BodyGraph API, this operation is `GET /v221006/hd-data` (base URL `https://api.bodygraphchart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-hd-data.md) for the provider-specific parameters and requirements.


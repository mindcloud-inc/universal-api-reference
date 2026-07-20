# Carbon Intensity: Get Regional Carbon Intensity Between Times By Postcode

Retrieves regional carbon intensity between datetimes by postcode.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-between-times-by-postcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-between-times-by-postcode?connectionId=$CONNECTION_ID&from=2026-04-12T12%3A00Z&to=2026-04-12T12%3A00Z&postcode=SW1A" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-12T12:00Z",
  "to": "2026-04-12T12:00Z",
  "postcode": "SW1A"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-between-times-by-postcode?${params}`, {
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
| `from` | string | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. Example: `2026-04-12T12:00Z`. |
| `to` | string | yes | Datetime in ISO-8601 format YYYY-MM-DDThh:mmZ exactly as required by the API path. Example: `2026-04-12T12:00Z`. |
| `postcode` | string | yes | Valid outward postcode such as SW1A, EH1, M1, or BS1. Example: `SW1A`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "data": [
            {
              "from": "string",
              "generationmix": [
                {
                  "fuel": "string",
                  "perc": 1
                }
              ],
              "intensity": {
                "actual": 1,
                "forecast": 1,
                "index": "string"
              },
              "to": "string"
            }
          ],
          "dnoregion": "string",
          "postcode": "string",
          "regionid": 1,
          "shortname": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].data` | array<object> |  |
| `data[].data[].from` | string |  |
| `data[].data[].generationmix` | array<object> |  |
| `data[].data[].generationmix[].fuel` | string |  |
| `data[].data[].generationmix[].perc` | number |  |
| `data[].data[].intensity` | object |  |
| `data[].data[].intensity.actual` | number |  |
| `data[].data[].intensity.forecast` | number |  |
| `data[].data[].intensity.index` | string |  |
| `data[].data[].to` | string |  |
| `data[].dnoregion` | string |  |
| `data[].postcode` | string |  |
| `data[].regionid` | number |  |
| `data[].shortname` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /regional/intensity/:from/:to/postcode/:postcode` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-regional-carbon-intensity-between-times-by-postcode.md) for the provider-specific parameters and requirements.


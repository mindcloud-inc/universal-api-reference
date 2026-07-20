# Carbon Intensity: Get Regional Carbon Intensity Forward 48 Hours

Retrieves 48-hour regional carbon intensity after a datetime.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-forward48-hours
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-forward48-hours?connectionId=$CONNECTION_ID&from=2026-04-12T12%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-12T12:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-forward48-hours?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "from": "string",
          "regions": [
            {
              "dnoregion": "string",
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
              "regionid": 1,
              "shortname": "Ava Chen"
            }
          ],
          "to": "string"
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
| `data[].from` | string |  |
| `data[].regions` | array<object> |  |
| `data[].regions[].dnoregion` | string |  |
| `data[].regions[].generationmix` | array<object> |  |
| `data[].regions[].generationmix[].fuel` | string |  |
| `data[].regions[].generationmix[].perc` | number |  |
| `data[].regions[].intensity` | object |  |
| `data[].regions[].intensity.actual` | number |  |
| `data[].regions[].intensity.forecast` | number |  |
| `data[].regions[].intensity.index` | string |  |
| `data[].regions[].regionid` | number |  |
| `data[].regions[].shortname` | string |  |
| `data[].to` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /regional/intensity/:from/fw48h` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-regional-carbon-intensity-forward48-hours.md) for the provider-specific parameters and requirements.


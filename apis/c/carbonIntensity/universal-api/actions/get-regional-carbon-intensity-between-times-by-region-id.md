# Carbon Intensity: Get Regional Carbon Intensity Between Times By Region ID

Retrieves regional carbon intensity between datetimes by region.

```
GET https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-between-times-by-region-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbon Intensity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-between-times-by-region-id?connectionId=$CONNECTION_ID&from=2026-04-12T12%3A00Z&to=2026-04-12T12%3A00Z&regionid=13" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-12T12:00Z",
  "to": "2026-04-12T12:00Z",
  "regionid": "13"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-regional-carbon-intensity-between-times-by-region-id?${params}`, {
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
| `regionid` | number | yes | Region ID defined by the Carbon Intensity API. Example: `13`. |

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
| `data[].regionid` | number |  |
| `data[].shortname` | string |  |

## Native endpoint

Through the native Carbon Intensity API, this operation is `GET /regional/intensity/:from/:to/regionid/:regionid` (base URL `https://api.carbonintensity.org.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-regional-carbon-intensity-between-times-by-region-id.md) for the provider-specific parameters and requirements.


# USGS Earthquake Hazards: Get Event API Parameters

Retrieves event API parameters from USGS Earthquake Hazards.

```
GET https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-event-api-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USGS Earthquake Hazards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-event-api-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSGSEarthquakeHazards/latest/actions/get-event-api-parameters?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "formats": [
        "string"
      ],
      "parameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formats` | array<string> | Supported response formats. |
| `parameters` | object | Known enumerated parameter values for the event interface. |

## Native endpoint

Through the native USGS Earthquake Hazards API, this operation is `GET /fdsnws/event/1/application.json` (base URL `https://earthquake.usgs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-api-parameters.md) for the provider-specific parameters and requirements.


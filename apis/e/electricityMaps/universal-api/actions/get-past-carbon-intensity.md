# Electricity Maps: Get Past Carbon Intensity



```
GET https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-past-carbon-intensity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Electricity Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-past-carbon-intensity?connectionId=$CONNECTION_ID&zone=string&datetime=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zone": "string",
  "datetime": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-past-carbon-intensity?${params}`, {
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
| `zone` | string | yes |  |
| `datetime` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_disclaimer": "string",
      "carbonIntensity": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datetime": "2026-05-07T12:00:00.000Z",
      "emissionFactorType": "string",
      "estimationMethod": "string",
      "isEstimated": true,
      "temporalGranularity": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_disclaimer` | string |  |
| `carbonIntensity` | number |  |
| `createdAt` | date |  |
| `datetime` | date |  |
| `emissionFactorType` | string |  |
| `estimationMethod` | string |  |
| `isEstimated` | boolean |  |
| `temporalGranularity` | string |  |
| `updatedAt` | date |  |
| `zone` | string |  |

## Native endpoint

Through the native Electricity Maps API, this operation is `GET /carbon-intensity/past` (base URL `https://api.electricitymaps.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-past-carbon-intensity.md) for the provider-specific parameters and requirements.


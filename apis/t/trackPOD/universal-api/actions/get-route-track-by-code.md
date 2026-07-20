# Track-POD: Get Route Track By Code

Retrieves route tracking details from Track-POD by code.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-route-track-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-route-track-by-code?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-route-track-by-code?${params}`, {
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
| `code` | string | yes | Route code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "TrackPoints": [
        {
          "Date": "2026-05-07T12:00:00.000Z",
          "Lat": 1,
          "Lng": 1,
          "Speed": 1
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
| `TrackPoints` | array<object> | List of track points |
| `TrackPoints[].Date` | date | Date |
| `TrackPoints[].Lat` | number | Latitude |
| `TrackPoints[].Lng` | number | Longitude |
| `TrackPoints[].Speed` | number | Speed, m/s |

## Native endpoint

Through the native Track-POD API, this operation is `GET /Route/Track/Code/:code` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-track-by-code.md) for the provider-specific parameters and requirements.


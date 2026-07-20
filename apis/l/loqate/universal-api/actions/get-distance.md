# Loqate: Get Distance

Retrieves the distance between locations from Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/get-distance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/get-distance?connectionId=$CONNECTION_ID&finish=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "finish": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/get-distance?${params}`, {
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
| `finish` | string | yes | The finish location or coordinates. |
| `start` | string | yes | The start location or coordinates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "segmentNumber": 1,
      "totalDistance": 1,
      "totalTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `segmentNumber` | number |  |
| `totalDistance` | number |  |
| `totalTime` | number |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /DistancesAndDirections/Interactive/Distance/v1.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-distance.md) for the provider-specific parameters and requirements.


# Transport for London: Get Line Arrivals At Stop

Retrieves line arrivals at a stop in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-arrivals-at-stop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-arrivals-at-stop?connectionId=$CONNECTION_ID&ids=string&stopPointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string",
  "stopPointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-arrivals-at-stop?${params}`, {
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
| `ids` | string | yes | Comma-separated TfL line IDs, such as victoria,circle. |
| `stopPointId` | string | yes | TfL stop point ID, such as 940GZZLUASL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destinationName": "Ava Chen",
      "expectedArrival": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lineId": "string",
      "lineName": "Ava Chen",
      "timeToStation": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destinationName` | string |  |
| `expectedArrival` | date |  |
| `id` | string |  |
| `lineId` | string |  |
| `lineName` | string |  |
| `timeToStation` | number |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/:ids/Arrivals/:stopPointId` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/line-arrivals-at-stop.md) for the provider-specific parameters and requirements.


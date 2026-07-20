# Transport for London: Get Line Route Sequence

Retrieves a line route sequence from Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-route-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-route-sequence?connectionId=$CONNECTION_ID&id=string&direction=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "direction": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-route-sequence?${params}`, {
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
| `id` | string | yes | Single TfL line ID, such as victoria. |
| `direction` | string | yes | Direction of travel: inbound, outbound, or all. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "direction": "string",
      "lineId": "string",
      "lineName": "Ava Chen",
      "orderedLineRoutes": [
        {}
      ],
      "stations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `direction` | string |  |
| `lineId` | string |  |
| `lineName` | string |  |
| `orderedLineRoutes` | array<object> |  |
| `stations` | array<object> |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/:id/Route/Sequence/:direction` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/line-route-sequence.md) for the provider-specific parameters and requirements.


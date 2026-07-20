# Transport for London: List Line Stop Points

Retrieves stop points served by a line in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-stop-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-stop-points?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-stop-points?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "commonName": "Ava Chen",
      "id": "string",
      "lat": 1,
      "lon": 1,
      "modes": [
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
| `commonName` | string |  |
| `id` | string |  |
| `lat` | number |  |
| `lon` | number |  |
| `modes` | array<string> |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/:id/StopPoints` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/line-stop-points.md) for the provider-specific parameters and requirements.


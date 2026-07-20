# Transport for London: Get Stop Points By Mode

Retrieves stop points for modes in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/stop-points-by-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/stop-points-by-mode?connectionId=$CONNECTION_ID&modes=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modes": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/stop-points-by-mode?${params}`, {
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
| `modes` | string | yes | Comma-separated mode names, such as tube,dlr,bus. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "pageSize": 1,
      "stopPoints": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `pageSize` | number |  |
| `stopPoints` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /StopPoint/Mode/:modes` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-points-by-mode.md) for the provider-specific parameters and requirements.


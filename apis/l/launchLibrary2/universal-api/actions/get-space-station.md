# Launch Library 2: Get Space Station



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-space-station
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-space-station?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-space-station?${params}`, {
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
| `id` | string | yes | Space station ID from Launch Library 2. Default: `8`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deorbited": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "founded": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "orbit": "string",
      "status": {
        "name": "Ava Chen"
      },
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deorbited` | date |  |
| `description` | string |  |
| `founded` | date |  |
| `id` | number |  |
| `name` | string |  |
| `orbit` | string |  |
| `status.name` | string |  |
| `type.name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET space_stations/{{id}}/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space-station.md) for the provider-specific parameters and requirements.


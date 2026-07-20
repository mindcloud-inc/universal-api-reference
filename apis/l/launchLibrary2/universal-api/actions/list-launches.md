# Launch Library 2: List Launches



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-launches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-launches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-launches?${params}`, {
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
| `search` | string | no | Search launch designator, provider, mission, launch, pad, rocket, or spacecraft fields. Example: `Starlink`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | no | Response detail level: list, normal, or detailed. One of: `0`, `1`, `2`. Default: `normal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "last_updated": "2026-05-07T12:00:00.000Z",
      "launch_designator": "string",
      "launch_service_provider": {
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "net": "2026-05-07T12:00:00.000Z",
      "response_mode": "string",
      "slug": "string",
      "status": {
        "name": "Ava Chen"
      },
      "url": "https://example.com",
      "window_end": "2026-05-07T12:00:00.000Z",
      "window_start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `last_updated` | date |  |
| `launch_designator` | string |  |
| `launch_service_provider.name` | string |  |
| `name` | string |  |
| `net` | date |  |
| `response_mode` | string |  |
| `slug` | string |  |
| `status.name` | string |  |
| `url` | string |  |
| `window_end` | date |  |
| `window_start` | date |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET launches/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-launches.md) for the provider-specific parameters and requirements.


# Launch Library 2: Get Launch



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-launch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-launch?connectionId=$CONNECTION_ID&id=e3df2ecd-c239-472f-95e4-2b89b4f75800" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e3df2ecd-c239-472f-95e4-2b89b4f75800"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-launch?${params}`, {
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
| `id` | string | yes | Launch UUID from Launch Library 2. Default: `e3df2ecd-c239-472f-95e4-2b89b4f75800`. Example: `e3df2ecd-c239-472f-95e4-2b89b4f75800`. |

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

Through the native Launch Library 2 API, this operation is `GET launches/{{id}}/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-launch.md) for the provider-specific parameters and requirements.


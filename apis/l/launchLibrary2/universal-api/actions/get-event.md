# Launch Library 2: Get Event



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-event?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/get-event?${params}`, {
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
| `id` | string | yes | Event ID from Launch Library 2. Default: `2`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "location": "string",
      "name": "Ava Chen",
      "slug": "string",
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com",
      "webcast_live": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `description` | string |  |
| `id` | number |  |
| `location` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `type.name` | string |  |
| `url` | string |  |
| `webcast_live` | boolean |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET events/{{id}}/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.


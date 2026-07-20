# Common Ninja: Get Widget

Retrieves a widget from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget?${params}`, {
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
| `id` | string | yes | The widget ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "data": {},
      "description": "string",
      "id": "string",
      "modelVersion": 1,
      "name": "Ava Chen",
      "previewImage": "string",
      "projectId": "string",
      "status": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `data` | object |  |
| `description` | string |  |
| `id` | string |  |
| `modelVersion` | number |  |
| `name` | string |  |
| `previewImage` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /widgets/:id` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget.md) for the provider-specific parameters and requirements.


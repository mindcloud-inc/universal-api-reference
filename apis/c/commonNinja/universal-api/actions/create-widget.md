# Common Ninja: Create Widget

Creates a widget in Common Ninja.

```
POST https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/create-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/create-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "status": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/create-widget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "status": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Widget data payload. |
| `description` | string | no | The widget description. |
| `modelVersion` | number | no | The widget data model version. |
| `name` | string | yes | The name of the widget. |
| `projectId` | string | no | The related project ID. |
| `status` | string | yes | The widget status: draft or published. |
| `type` | string | yes | The widget type to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "data": {},
      "description": "string",
      "editorUrl": "https://example.com",
      "embedCode": {},
      "id": "string",
      "modelVersion": 1,
      "name": "Ava Chen",
      "previewImage": "string",
      "projectId": "string",
      "slug": "string",
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
| `editorUrl` | string |  |
| `embedCode` | object |  |
| `id` | string |  |
| `modelVersion` | number |  |
| `name` | string |  |
| `previewImage` | string |  |
| `projectId` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Common Ninja API, this operation is `POST /widgets` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-widget.md) for the provider-specific parameters and requirements.


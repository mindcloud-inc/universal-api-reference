# Common Ninja: Update Widget

Updates a widget in Common Ninja.

```
PUT https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/update-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/update-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/update-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Updated widget data payload. |
| `description` | string | no | The updated widget description. |
| `id` | string | yes | The widget ID. |
| `name` | string | no | The updated widget name. |
| `status` | string | no | The updated widget status: draft or published. |

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

Through the native Common Ninja API, this operation is `PUT /widgets/:id` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-widget.md) for the provider-specific parameters and requirements.


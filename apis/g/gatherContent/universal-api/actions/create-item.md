# GatherContent: Create Item

Creates a new item in GatherContent.

```
POST https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folder_uuid": "string",
  "project_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folder_uuid": "string",
    "project_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folder_uuid` | string | yes | Destination folder UUID. |
| `project_id` | string | yes | Project id. |
| `template_id` | string | no | Template ID to attach. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GatherContent API, this operation is `POST /projects/:project_id/items` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.


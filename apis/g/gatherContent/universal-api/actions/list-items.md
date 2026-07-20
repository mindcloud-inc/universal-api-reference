# GatherContent: List Items

Lists items in a GatherContent project.

```
GET https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/list-items?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/list-items?${params}`, {
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
| `project_id` | string | yes | Project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder_uuid": "string",
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "status_id": 1,
      "template_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder_uuid` | string |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `status_id` | number |  |
| `template_id` | number |  |

## Native endpoint

Through the native GatherContent API, this operation is `GET /projects/:project_id/items` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.


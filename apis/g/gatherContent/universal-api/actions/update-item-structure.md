# GatherContent: Update Item Structure

Updates the structure of an item in GatherContent.

```
PUT https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/update-item-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/update-item-structure" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groups[]": [
    {}
  ],
  "item_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/update-item-structure', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groups[]": [{}],
    "item_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groups[]` | array<object> | yes | Structure groups definition. |
| `item_id` | string | yes | Item ID. |

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

Through the native GatherContent API, this operation is `PUT /items/:item_id/structure` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-structure.md) for the provider-specific parameters and requirements.


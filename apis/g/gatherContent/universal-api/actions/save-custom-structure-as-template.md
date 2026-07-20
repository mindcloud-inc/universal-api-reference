# GatherContent: Save Custom Structure As Template

Creates a template from an item's custom structure in GatherContent.

```
POST https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/save-custom-structure-as-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/save-custom-structure-as-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item_id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/save-custom-structure-as-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item_id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item_id` | string | yes | Item ID. |
| `name` | string | yes | Template name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "number_of_items_using": 1,
      "project_id": 1,
      "structure_uuid": "string",
      "updated_at": "string",
      "updated_by": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `number_of_items_using` | number |  |
| `project_id` | number |  |
| `structure_uuid` | string |  |
| `updated_at` | string |  |
| `updated_by` | number |  |

## Native endpoint

Through the native GatherContent API, this operation is `POST /items/:item_id/save_as_template` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-custom-structure-as-template.md) for the provider-specific parameters and requirements.


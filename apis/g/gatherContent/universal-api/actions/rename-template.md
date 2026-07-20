# GatherContent: Rename Template

Renames an existing template in GatherContent.

```
PUT https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/rename-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/rename-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/rename-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Template name. |
| `template_id` | string | yes | Template ID. |

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

Through the native GatherContent API, this operation is `POST /templates/:template_id/rename` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-template.md) for the provider-specific parameters and requirements.


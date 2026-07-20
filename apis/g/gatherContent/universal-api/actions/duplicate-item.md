# GatherContent: Duplicate Item

Duplicates an existing item in GatherContent.

```
POST https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/duplicate-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/duplicate-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/duplicate-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native GatherContent API, this operation is `POST /items/:item_id/duplicate` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-item.md) for the provider-specific parameters and requirements.


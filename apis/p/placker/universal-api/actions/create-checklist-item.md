# Placker: Create Checklist Item



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-checklist-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-checklist-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklist": "sjwa8k5le5p1c",
  "title": "New checklist item"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-checklist-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklist": "sjwa8k5le5p1c",
    "title": "New checklist item"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklist` | string | yes | Checklist ID. Example: `sjwa8k5le5p1c`. |
| `title` | string | yes | Title of the checklist item. Example: `New checklist item`. |
| `position` | number | no | Position of the item in the checklist. Example: `1000`. |
| `members[]` | array<object> | no | Members to assign to the item as an array of objects with id fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The ID of the created checklist item. |
| `status` | string | Operation status. |

## Native endpoint

Through the native Placker API, this operation is `POST /checklist/:checklist/item` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checklist-item.md) for the provider-specific parameters and requirements.


# Placker: Update Checklist Item



```
PUT https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-checklist-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-checklist-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklist": "sjwa8k5le5p1c",
  "item": "1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/update-checklist-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklist": "sjwa8k5le5p1c",
    "item": "1234567890"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklist` | string | yes | Checklist ID. Example: `sjwa8k5le5p1c`. |
| `item` | string | yes | Checklist item ID. Example: `1234567890`. |
| `title` | string | no | Title of the checklist item. Example: `Updated checklist item`. |
| `description` | string | no | Description of the checklist item. Example: `Detailed description`. |
| `status` | string | no | Status of the checklist item. Example: `INPROGRESS`. |
| `startDates` | object | no | Planned and actual start dates. |
| `endDates` | object | no | Planned and actual end dates. |
| `effort` | object | no | Planned and actual effort values. |
| `duration` | number | no | Duration in seconds. Example: `3600`. |
| `trafficLight` | string | no | Traffic light status. Example: `amber`. |
| `membersAdd[]` | array<object> | no | Members to add to the item as an array of objects with id fields. |
| `membersRemove[]` | array<object> | no | Members to remove from the item as an array of objects with id fields. |
| `position` | number | no | Position of the item in the checklist. Example: `2000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Operation status. |

## Native endpoint

Through the native Placker API, this operation is `PATCH /checklist/:checklist/item/:item` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-checklist-item.md) for the provider-specific parameters and requirements.


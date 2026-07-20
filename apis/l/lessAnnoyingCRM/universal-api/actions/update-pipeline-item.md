# Less Annoying CRM: Update Pipeline Item



```
PUT https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-pipeline-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-pipeline-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipelineItemId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-pipeline-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipelineItemId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipelineItemId` | string | yes | The pipeline item Id to update. |
| `statusId` | string | no | Updated status Id for the item. |
| `note` | string | no | Optional history note for the status change. |
| `runStatusAutomation` | boolean | no | Whether to run the status automation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Less Annoying CRM API returns.

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pipeline-item.md) for the provider-specific parameters and requirements.


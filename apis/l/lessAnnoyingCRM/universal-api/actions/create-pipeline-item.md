# Less Annoying CRM: Create Pipeline Item



```
POST https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/create-pipeline-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/create-pipeline-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "pipelineId": "string",
  "statusId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/create-pipeline-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "pipelineId": "string",
    "statusId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The contact Id this pipeline item will attach to. |
| `pipelineId` | string | yes | The pipeline Id to add the item to. |
| `statusId` | string | yes | The status Id where the item should start. |
| `note` | string | no | Optional history note for the pipeline item. |
| `runStatusAutomation` | boolean | no | Whether to run the status automation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pipelineItemId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pipelineItemId` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pipeline-item.md) for the provider-specific parameters and requirements.


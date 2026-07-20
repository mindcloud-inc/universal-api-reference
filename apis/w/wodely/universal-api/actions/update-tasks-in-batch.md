# Wodely: Update Tasks in Batch



```
PUT https://connect.mindcloud.co/v1/universal/wodely/latest/actions/update-tasks-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/update-tasks-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskGuidList": "DD2A6408A6,E96CB4F5D6",
  "fieldName": "ExternalKey"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/update-tasks-in-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskGuidList": "DD2A6408A6,E96CB4F5D6",
    "fieldName": "ExternalKey"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskGuidList` | string | yes | Provide one or more Task IDs, separated by commas. Example: `DD2A6408A6,E96CB4F5D6`. |
| `fieldName` | string | yes | Supported fields include Priority, TaskDesc, Requirements, ExternalKey, AmountDue, DeliveryFee, ServiceTime, Capacity, Skills, TemplateId, MerchantId, AfterDateTime, BeforeDateTime, Tag1, Tag2, Tag3, Tag4, Tag5. Example: `ExternalKey`. |
| `fieldValue` | string | no | The new value to apply to the selected field. Example: `mindcloud-updated-key`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/tasks/bulkupdate` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tasks-in-batch.md) for the provider-specific parameters and requirements.


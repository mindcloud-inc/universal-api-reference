# Lasso X: Create Reporting Batch

Creates a reporting batch in Lasso X.

```
POST https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/create-reporting-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/create-reporting-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch_name": "Ava Chen",
  "type": "string",
  "format": "string",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/create-reporting-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch_name": "Ava Chen",
    "type": "string",
    "format": "string",
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch_name` | string | yes | Name of the reporting batch. |
| `type` | string | yes | Report type, for example Revision. |
| `format` | string | yes | Required report filename format. Supports Lasso variables such as {cvr}, {name}, {type}, {rundate}, and {balanceday}. |
| `items[]` | array<object> | yes | Reports to generate in the batch. Each item must include cvr and may include format and internalCustomerId. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notification_email` | string | no | Optional email for report completion notifications. |
| `notification_webhook_url` | string | no | Optional webhook URL for report completion notifications. |
| `scheduled_time` | date | no | Optional scheduled time for the batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "batchSize": 1,
      "completionPercentage": 1,
      "emailFormat": "ava@example.com",
      "id": "string",
      "lassoOrgId": "string",
      "lassoUserId": "string",
      "name": "Ava Chen",
      "notificationEmail": "ava@example.com",
      "notificationWebHookUrl": "https://example.com",
      "scheduledTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `batchSize` | number |  |
| `completionPercentage` | number |  |
| `emailFormat` | string |  |
| `id` | string |  |
| `lassoOrgId` | string |  |
| `lassoUserId` | string |  |
| `name` | string |  |
| `notificationEmail` | string |  |
| `notificationWebHookUrl` | string |  |
| `scheduledTime` | date |  |
| `status` | string |  |
| `timestamp` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `POST /apps/reporting/batches` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reporting-batch.md) for the provider-specific parameters and requirements.


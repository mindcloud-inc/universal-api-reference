# Lasso X: Get Reporting Batch

Retrieves a reporting batch from Lasso X by ID.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-reporting-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-reporting-batch?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/get-reporting-batch?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Reporting batch ID. |

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

Through the native Lasso X API, this operation is `GET /apps/reporting/batches/:id` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reporting-batch.md) for the provider-specific parameters and requirements.


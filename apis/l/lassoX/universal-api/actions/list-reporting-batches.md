# Lasso X: List Reporting Batches

Retrieves reporting batches from Lasso X.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batches?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "archived": true,
          "batchSize": 1,
          "completionPercentage": 1,
          "emailFormat": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "notificationEmail": "ava@example.com",
          "notificationWebHookUrl": "https://example.com",
          "scheduledTime": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "timestamp": "2026-05-07T12:00:00.000Z",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].archived` | boolean |  |
| `[].batchSize` | number |  |
| `[].completionPercentage` | number |  |
| `[].emailFormat` | string |  |
| `[].id` | string |  |
| `[].name` | string |  |
| `[].notificationEmail` | string |  |
| `[].notificationWebHookUrl` | string |  |
| `[].scheduledTime` | date |  |
| `[].status` | string |  |
| `[].timestamp` | date |  |
| `[].type` | string |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /apps/reporting/batches` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reporting-batches.md) for the provider-specific parameters and requirements.


# TMetric: List Recent Tasks



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-recent-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-recent-tasks?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-recent-tasks?${params}`, {
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
| `accountId` | number | yes | Workspace identifier. |
| `userId` | number | no | Optional user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isBillable": true,
      "isNew": true,
      "name": "Ava Chen",
      "project": {
        "iconUrl": "https://example.com",
        "id": 1,
        "invoiceMethod": "string",
        "isBillable": true,
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isBillable` | boolean |  |
| `isNew` | boolean |  |
| `name` | string |  |
| `project.iconUrl` | string |  |
| `project.id` | number |  |
| `project.invoiceMethod` | string |  |
| `project.isBillable` | boolean |  |
| `project.name` | string |  |
| `project.status` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/tasks/recent` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-tasks.md) for the provider-specific parameters and requirements.


# TMetric: List Trackable Projects



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-trackable-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-trackable-projects?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-trackable-projects?${params}`, {
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
      "iconUrl": "https://example.com",
      "id": 1,
      "invoiceMethod": "string",
      "isBillable": true,
      "name": "Ava Chen",
      "recentUsageTime": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iconUrl` | string |  |
| `id` | number |  |
| `invoiceMethod` | string |  |
| `isBillable` | boolean |  |
| `name` | string |  |
| `recentUsageTime` | date |  |
| `status` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/timeentries/projects` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trackable-projects.md) for the provider-specific parameters and requirements.


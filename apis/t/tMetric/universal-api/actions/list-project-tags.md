# TMetric: List Project Tags



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-project-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-project-tags?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-project-tags?${params}`, {
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
| `projectId` | number | no | Project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isWorkType": true,
      "isWorkTypeBillable": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isWorkType` | boolean |  |
| `isWorkTypeBillable` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/timeentries/tags` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-tags.md) for the provider-specific parameters and requirements.


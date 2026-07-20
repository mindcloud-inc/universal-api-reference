# ActiveCollab: List Project Time Records

Retrieves time records for a project in ActiveCollab.

```
GET https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-project-time-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCollab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-project-time-records?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-project-time-records?${params}`, {
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
| `projectId` | string | yes | The ActiveCollab project ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCollab API returns.

## Native endpoint

Through the native ActiveCollab API, this operation is `GET /projects/:projectId/time-records` (base URL `https://app.activecollab.com/:instanceId/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-time-records.md) for the provider-specific parameters and requirements.


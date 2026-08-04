# D-Tools SI: List Subscribed Projects



```
GET https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/list-subscribed-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D-Tools SI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/list-subscribed-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/list-subscribed-projects?${params}`, {
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
| `projects` | string | no |  |
| `totalCount` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native D-Tools SI API returns.

## Native endpoint

Through the native D-Tools SI API, this operation is `GET Subscribe/Projects` (base URL `https://api.d-tools.com/SI/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribed-projects.md) for the provider-specific parameters and requirements.


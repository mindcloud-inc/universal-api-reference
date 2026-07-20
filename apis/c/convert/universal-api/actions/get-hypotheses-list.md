# Convert: List Hypotheses

Retrieves hypotheses from a Convert project.

```
GET https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-hypotheses-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-hypotheses-list?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convert/latest/actions/get-hypotheses-list?${params}`, {
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
| `projectId` | string | yes | Convert project ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Convert API returns.

## Native endpoint

Through the native Convert API, this operation is `POST /accounts/:account_id/projects/:project_id/hypotheses` (base URL `https://api.convert.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hypotheses-list.md) for the provider-specific parameters and requirements.


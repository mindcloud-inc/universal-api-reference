# Procore: List Drawing Areas

Retrieves drawing areas from Procore.

```
GET https://connect.mindcloud.co/v1/universal/procore/latest/actions/list-drawing-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Procore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/procore/latest/actions/list-drawing-areas?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/procore/latest/actions/list-drawing-areas?${params}`, {
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
| `projectId` | string | yes | Unique identifier for the project. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Procore API returns.

## Native endpoint

Through the native Procore API, this operation is `GET /rest/v1.1/projects/:project_id/drawing_areas` (base URL `https://api.procore.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-drawing-areas.md) for the provider-specific parameters and requirements.


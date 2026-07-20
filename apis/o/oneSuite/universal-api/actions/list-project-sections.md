# OneSuite: List Project Sections

Retrieves sections for a project in OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-project-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-project-sections?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-project-sections?${params}`, {
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
| `projectId` | string | yes | The ID of the project |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/projects/:project_id/sections` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-sections.md) for the provider-specific parameters and requirements.


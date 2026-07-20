# FTrack: Search Entities

Searches entities in FTrack by terms and entity type.

```
GET https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/search-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/search-entities?connectionId=$CONNECTION_ID&expression=project.name%20is%20%22Demo%20Project%22&terms%5B%5D=string&entityType=Task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expression": "project.name is \"Demo Project\"",
  "terms[]": "string",
  "entityType": "Task"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/search-entities?${params}`, {
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
| `expression` | string | yes | Search expression to scope the results. Example: `project.name is "Demo Project"`. |
| `terms[]` | array<string> | yes | Search terms as a list of strings. |
| `entityType` | string | yes | Entity type to search, such as Task or AssetVersion. Example: `Task`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-entities.md) for the provider-specific parameters and requirements.


# Bridgit Bench: List Account Project Field Values



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-project-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-project-field-values?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-project-field-values?${params}`, {
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
| `id` | number | yes | The Account ID |
| `projectIds` | number | no | Optional paramater of comma delimited ids for filtering results based on the project IDs provided Accepts multiple values in one string, delimited by `,`. |
| `projectNumber` | string | no | Optional - for filtering result by system field "Project Number" |
| `externalId` | string | no | Optional - for filtering result by system field "External ID" |
| `classification` | list<string> | no | Optional - for filtering result by classification: All or Experience" One of: `All`, `Experience`. Default: `All`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeEmpty` | boolean | no | If true, the response will include all project field values, even if no value is set for a given field. If false, field values that are empty are not included in the response. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/Accounts/:id/project-field-values` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-project-field-values.md) for the provider-specific parameters and requirements.


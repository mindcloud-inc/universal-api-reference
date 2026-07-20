# Harness: List Pipelines

Retrieves pipelines from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-pipelines?${params}`, {
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
| `deployment_type` | string | no | Deployment type to filter pipelines by. |
| `description` | string | no | Filter by pipeline description. |
| `env_names` | list<string> | no | Environment names to filter pipelines by. |
| `filter_identifier` | string | no | Saved filter identifier. |
| `module` | string | no | Harness module included in the pipeline. |
| `name` | string | no | Filter by pipeline name. |
| `order` | string | no | Sort direction. |
| `pipeline_identifiers` | list<string> | no | Pipeline identifiers to include. |
| `repository` | string | no | Repository name to filter pipelines by. |
| `search_term` | string | no | Filter pipelines matching the search term. |
| `service_names` | list<string> | no | Service names to filter pipelines by. |
| `sort` | string | no | Field used for sorting. |
| `tags` | string | no | Filter by tags using key:value syntax. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "identifier": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Pipeline description. |
| `identifier` | string | Pipeline identifier. |
| `name` | string | Pipeline name. |

## Native endpoint

Through the native Harness API, this operation is `GET /v1/orgs/:orgIdentifier/projects/:projectIdentifier/pipelines` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.


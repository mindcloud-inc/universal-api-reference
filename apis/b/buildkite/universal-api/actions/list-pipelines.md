# Buildkite: List Pipelines

Retrieves pipelines from Buildkite.

```
GET https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-pipelines?connectionId=$CONNECTION_ID&limit=25&offset=0&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-pipelines?${params}`, {
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
| `organization` | string | yes | The Buildkite organization slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "repository": "string",
      "slug": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `repository` | string |  |
| `slug` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `GET /organizations/:organization/pipelines` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.


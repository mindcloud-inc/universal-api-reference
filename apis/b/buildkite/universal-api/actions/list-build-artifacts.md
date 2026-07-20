# Buildkite: List Build Artifacts

Retrieves build artifacts from Buildkite.

```
GET https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-build-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-build-artifacts?connectionId=$CONNECTION_ID&limit=25&offset=0&build=string&organization=string&pipeline=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "build": "string",
  "organization": "string",
  "pipeline": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-build-artifacts?${params}`, {
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
| `build` | string | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com",
      "fileSize": 1,
      "id": "string",
      "path": "string",
      "sha1sum": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string |  |
| `fileSize` | number |  |
| `id` | string |  |
| `path` | string |  |
| `sha1sum` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `GET /organizations/:organization/pipelines/:pipeline/builds/:build/artifacts` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-build-artifacts.md) for the provider-specific parameters and requirements.


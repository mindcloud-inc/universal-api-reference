# Buildkite: Get Pipeline

Retrieves a pipeline from Buildkite.

```
GET https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-pipeline?connectionId=$CONNECTION_ID&organization=string&pipeline=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "pipeline": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-pipeline?${params}`, {
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
| `pipeline` | string | yes | The Buildkite pipeline slug. |

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

Through the native Buildkite API, this operation is `GET /organizations/:organization/pipelines/:pipeline` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline.md) for the provider-specific parameters and requirements.


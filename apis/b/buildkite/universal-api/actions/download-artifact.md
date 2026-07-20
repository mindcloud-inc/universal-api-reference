# Buildkite: Download Artifact

Downloads an artifact from Buildkite.

```
GET https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/download-artifact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/download-artifact?connectionId=$CONNECTION_ID&artifact=string&build=string&job=string&organization=string&pipeline=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "artifact": "string",
  "build": "string",
  "job": "string",
  "organization": "string",
  "pipeline": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/download-artifact?${params}`, {
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
| `artifact` | string | yes | The Buildkite artifact UUID. |
| `build` | string | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `job` | string | yes | The Buildkite job UUID. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "downloadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `downloadUrl` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `GET /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/artifacts/:artifact/download` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-artifact.md) for the provider-specific parameters and requirements.


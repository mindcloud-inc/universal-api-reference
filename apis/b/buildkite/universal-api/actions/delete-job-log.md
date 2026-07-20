# Buildkite: Delete Job Log

Deletes a job log from Buildkite.

```
DELETE https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/delete-job-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/delete-job-log?connectionId=$CONNECTION_ID&build=string&job=string&organization=string&pipeline=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "build": "string",
  "job": "string",
  "organization": "string",
  "pipeline": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/delete-job-log?${params}`, {
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
| `job` | string | yes | The Buildkite job UUID. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Buildkite API, this operation is `DELETE /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/log` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job-log.md) for the provider-specific parameters and requirements.


# Buildkite: Reprioritize Job

Reprioritizes an existing job in Buildkite.

```
PUT https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/reprioritize-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/reprioritize-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "build": "string",
  "job": "string",
  "organization": "string",
  "pipeline": "string",
  "priority": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/reprioritize-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "build": "string",
    "job": "string",
    "organization": "string",
    "pipeline": "string",
    "priority": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `build` | string | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `job` | string | yes | The Buildkite job UUID. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |
| `priority` | string | yes | The new priority for the job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "state": "string",
      "type": "string",
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
| `state` | string |  |
| `type` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/reprioritize` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reprioritize-job.md) for the provider-specific parameters and requirements.


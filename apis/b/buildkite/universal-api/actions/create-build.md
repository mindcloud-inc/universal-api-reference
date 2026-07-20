# Buildkite: Create Build

Creates a new build in Buildkite.

```
POST https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/create-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/create-build" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branch": "string",
  "commit": "string",
  "organization": "string",
  "pipeline": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/create-build', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branch": "string",
    "commit": "string",
    "organization": "string",
    "pipeline": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch` | string | yes | The branch name for the new build. |
| `commit` | string | yes | The commit SHA to build. |
| `message` | string | no | An optional message for the new build. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "commit": "string",
      "createdAt": "string",
      "id": "string",
      "message": "string",
      "number": 1,
      "state": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `commit` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `message` | string |  |
| `number` | number |  |
| `state` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `POST /organizations/:organization/pipelines/:pipeline/builds` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-build.md) for the provider-specific parameters and requirements.


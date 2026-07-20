# Buildkite: Cancel Build

Cancels an existing build in Buildkite.

```
PUT https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/cancel-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/cancel-build" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "build": "string",
  "organization": "string",
  "pipeline": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/cancel-build', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "build": "string",
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
| `build` | string | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
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
| `id` | string |  |
| `number` | number |  |
| `state` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `PUT /organizations/:organization/pipelines/:pipeline/builds/:build/cancel` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-build.md) for the provider-specific parameters and requirements.


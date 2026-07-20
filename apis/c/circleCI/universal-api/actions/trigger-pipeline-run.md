# CircleCI: Trigger Pipeline Run



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/trigger-pipeline-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/trigger-pipeline-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/trigger-pipeline-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkout` | object | no | Checkout configuration. |
| `config` | object | no | Config overrides. |
| `definition_id` | string | no | Pipeline definition identifier to run. |
| `organization` | string | no | VCS organization name. |
| `parameters` | object | no | Pipeline parameters. |
| `project` | string | no | Repository name. |
| `provider` | string | no | VCS provider, for example github or bitbucket. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "number": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `number` | number |  |
| `state` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /project/:provider/:organization/:project/pipeline/run` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-pipeline-run.md) for the provider-specific parameters and requirements.


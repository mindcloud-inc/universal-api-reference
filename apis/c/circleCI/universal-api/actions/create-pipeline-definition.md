# CircleCI: Create Pipeline Definition



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-pipeline-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-pipeline-definition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-pipeline-definition', {
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
| `checkout_source` | string | no | Repository checkout source configuration. |
| `config_source` | string | no | Pipeline configuration source. |
| `description` | string | no | Pipeline definition description. |
| `name` | string | no | Pipeline definition name. |
| `project_id` | string | no | Opaque project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configSource": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configSource` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /projects/:project_id/pipeline-definitions` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pipeline-definition.md) for the provider-specific parameters and requirements.


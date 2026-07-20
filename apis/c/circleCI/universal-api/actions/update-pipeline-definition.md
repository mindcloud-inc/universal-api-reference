# CircleCI: Update Pipeline Definition



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-pipeline-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-pipeline-definition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/update-pipeline-definition', {
  method: 'PUT',
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
| `pipeline_definition_id` | string | no | Opaque pipeline definition identifier. |
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

Through the native CircleCI API, this operation is `PATCH /projects/:project_id/pipeline-definitions/:pipeline_definition_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pipeline-definition.md) for the provider-specific parameters and requirements.


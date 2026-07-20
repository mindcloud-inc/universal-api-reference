# Porsline: Create Variables



```
POST https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "survey_id": 1,
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-variables', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "survey_id": 1,
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `survey_id` | number | yes | The id of the target survey. |
| `variables` | list<object> | yes | List of variable objects. Each item should include name, variableSource, type, and optionally hasResponse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `variables` | array<object> |  |

## Native endpoint

Through the native Porsline API, this operation is `POST /api/surveys/:survey_id/variables/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-variables.md) for the provider-specific parameters and requirements.


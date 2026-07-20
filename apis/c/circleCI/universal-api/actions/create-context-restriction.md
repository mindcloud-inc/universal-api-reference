# CircleCI: Create Context Restriction



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-context-restriction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-context-restriction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "restrictionType": "string",
  "restrictionValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-context-restriction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "restrictionType": "string",
    "restrictionValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `restrictionType` | string | yes | Restriction type: project, expression, or group. |
| `restrictionValue` | string | yes | Restriction value for the chosen restriction type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "restrictionType": "string",
      "restrictionValue": "string"
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
| `projectId` | string |  |
| `restrictionType` | string |  |
| `restrictionValue` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /context/:context_id/restrictions` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-context-restriction.md) for the provider-specific parameters and requirements.


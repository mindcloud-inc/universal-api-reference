# Week Plan: Create Action



```
POST https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Date` | string | no | Optional target date in YYYY-MM-DD format. |
| `Quadrant` | number | no | Optional Eisenhower quadrant for the new action. |
| `RoleId` | number | no | Optional role assignment for the new action. |
| `Text` | string | yes | Task text, including any Week Plan markdown prefixes such as #. |
| `WorkspaceId` | number | no | Optional workspace override for the new action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Data": {},
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Data` | object |  |
| `Message` | string |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST actions` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.


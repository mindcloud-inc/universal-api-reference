# Microsoft 365 Planner: Create Plan



```
POST https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Product launch plan",
  "container.url": "https://graph.microsoft.com/v1.0/groups/9b1f3c7a-1234-4abc-9def-123456789abc"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/create-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Product launch plan",
    "container.url": "https://graph.microsoft.com/v1.0/groups/9b1f3c7a-1234-4abc-9def-123456789abc"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the new Planner plan. Example: `Product launch plan`. |
| `container.url` | string | yes | Microsoft Graph URL for the plan container, such as https://graph.microsoft.com/v1.0/groups/{group-id}. Example: `https://graph.microsoft.com/v1.0/groups/9b1f3c7a-1234-4abc-9def-123456789abc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "owner": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date |  |
| `id` | string |  |
| `owner` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `POST /v1.0/planner/plans` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-plan.md) for the provider-specific parameters and requirements.


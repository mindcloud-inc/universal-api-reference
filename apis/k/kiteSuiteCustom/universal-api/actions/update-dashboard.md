# Kite Suite: Update Dashboard



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "name": "Ava Chen",
  "privacy": "string",
  "widgetName": "Ava Chen",
  "type": "string",
  "project": "string",
  "sprint": "string",
  "lists[]": [
    "string"
  ],
  "estimateBy": "string",
  "groupBy": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-dashboard', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "name": "Ava Chen",
    "privacy": "string",
    "widgetName": "Ava Chen",
    "type": "string",
    "project": "string",
    "sprint": "string",
    "lists[]": ["string"],
    "estimateBy": "string",
    "groupBy": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | dashboardID |
| `body` | object | yes | Request body |
| `name` | string | yes |  |
| `privacy` | string | yes |  |
| `widgetName` | string | yes |  |
| `type` | string | yes |  |
| `project` | string | yes |  |
| `sprint` | string | yes |  |
| `lists[]` | array | yes |  |
| `estimateBy` | string | yes |  |
| `groupBy` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createAt": "string",
      "layout": "string",
      "name": "Ava Chen",
      "owner": "string",
      "privacy": "string",
      "updatedAt": "string",
      "widgets": [
        "string"
      ],
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The auto-generated id of the dashboard |
| `createAt` | string | Creation time of dashboard |
| `layout` | string | Layout selected |
| `name` | string | Name of dashboard |
| `owner` | string | Owner of dashboard |
| `privacy` | string | Privacy of dashboard |
| `updatedAt` | string | Updated time of dashboard |
| `widgets` | array | Widgets of dashboard |
| `workspace` | string | Workspace of dashboard |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/dashboard/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dashboard.md) for the provider-specific parameters and requirements.


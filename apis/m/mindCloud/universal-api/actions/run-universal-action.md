# MindCloud: Run Universal Action



```
POST https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/run-universal-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/run-universal-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionSlug": "string",
  "appSlug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/run-universal-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionSlug": "string",
    "appSlug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionSlug` | string | yes | Action Slug for this MindCloud v2 request. |
| `appSlug` | string | yes | App Slug for this MindCloud v2 request. |
| `arguments` | object | no | Arguments for this MindCloud v2 request. |
| `connectionId` | string | no | Connection ID for this MindCloud v2 request. |
| `fields` | string | no | Fields for this MindCloud v2 request. |
| `options` | object | no | Options for this MindCloud v2 request. |
| `sort` | string | no | Sort for this MindCloud v2 request. |
| `version` | string | no | Version for this MindCloud v2 request. |
| `where` | string | no | Where for this MindCloud v2 request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MindCloud API returns.

## Native endpoint

Through the native MindCloud API, this operation is `POST /v2/universal/apps/:appSlug/actions/:actionSlug/run` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-universal-action.md) for the provider-specific parameters and requirements.


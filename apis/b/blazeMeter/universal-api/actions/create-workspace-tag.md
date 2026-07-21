# BlazeMeter: Create Workspace Tag

Creates a workspace tag in BlazeMeter.

```
POST https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/create-workspace-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlazeMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/create-workspace-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/create-workspace-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider response payload. |
| `id` | string | Optional response identifier. |
| `message` | string | Optional response message. |
| `meta` | object | Execution metadata including request/response details. |
| `success` | boolean | Whether the action run succeeded. |

## Native endpoint

Through the native BlazeMeter API, this operation is `POST /workspaces/:workspaceId/tags` (base URL `https://a.blazemeter.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-tag.md) for the provider-specific parameters and requirements.


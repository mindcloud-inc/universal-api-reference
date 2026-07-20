# Asana: Submit parallel requests

Submits parallel API requests to Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/submit-parallel-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/submit-parallel-requests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataActions][]": [
    "string"
  ],
  "dataActionsData": {},
  "dataActionsMethod": "string",
  "dataActionsOptionsFields": "string",
  "dataActionsOptionsLimit": 1,
  "dataActionsOptionsOffset": 1,
  "dataActionsRelativePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/submit-parallel-requests', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataActions][]": ["string"],
    "dataActionsData": {},
    "dataActionsMethod": "string",
    "dataActionsOptionsFields": "string",
    "dataActionsOptionsLimit": 1,
    "dataActionsOptionsOffset": 1,
    "dataActionsRelativePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataActions][]` | array | yes |  |
| `dataActionsData` | object | yes |  |
| `dataActionsMethod` | string | yes |  |
| `dataActionsOptionsFields` | list | yes |  |
| `dataActionsOptionsLimit` | number | yes |  |
| `dataActionsOptionsOffset` | number | yes |  |
| `dataActionsRelativePath` | string | yes |  |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |
| `data.actions` | list<string> | no | Asana actions parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST batch` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-parallel-requests.md) for the provider-specific parameters and requirements.


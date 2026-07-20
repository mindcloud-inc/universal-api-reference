# Asana: Move or Insert sections

Moves or inserts sections in an Asana project.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/move-or-insert-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/move-or-insert-sections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataAfterSection": "string",
  "dataBeforeSection": "string",
  "dataProject": "string",
  "dataSection": "string",
  "projectGid": "string",
  "data.section": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/move-or-insert-sections', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataAfterSection": "string",
    "dataBeforeSection": "string",
    "dataProject": "string",
    "dataSection": "string",
    "projectGid": "string",
    "data.section": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataAfterSection` | string | yes |  |
| `dataBeforeSection` | string | yes |  |
| `dataProject` | string | yes |  |
| `dataSection` | string | yes |  |
| `projectGid` | string | yes | Asana project gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `data.section` | string | yes | Asana section parameter. |
| `data.before_section` | string | no | Asana before section parameter. |
| `data.after_section` | string | no | Asana after section parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST projects/:project_gid/sections/insert` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-or-insert-sections.md) for the provider-specific parameters and requirements.


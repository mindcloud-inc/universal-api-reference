# Asana: Add a custom field to a project

Adds a custom field to a project in Asana.

```
PUT https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-custom-field-to-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-custom-field-to-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataCustomField": "string",
  "dataInsertAfter": "string",
  "dataInsertBefore": "string",
  "dataIsImportant": true,
  "projectGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-custom-field-to-a-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataCustomField": "string",
    "dataInsertAfter": "string",
    "dataInsertBefore": "string",
    "dataIsImportant": true,
    "projectGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataCustomField` | string | yes |  |
| `dataInsertAfter` | string | yes |  |
| `dataInsertBefore` | string | yes |  |
| `dataIsImportant` | boolean | yes |  |
| `projectGid` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST projects/:project_gid/addCustomFieldSetting` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-custom-field-to-a-project.md) for the provider-specific parameters and requirements.


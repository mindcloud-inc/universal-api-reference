# Docupilot: Update Template

Updates an existing template in Docupilot.

```
PUT https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "preferences.info": {},
  "folder.name": "Ava Chen",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "preferences.info": {},
    "folder.name": "Ava Chen",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `preferences.info` | object | yes |  |
| `folder.name` | string | yes |  |
| `title` | string | yes |  |
| `preferences.autoNumber` | number | no |  |
| `description` | string | no |  |
| `documentStatus` | list | no | One of: `active`, `test`. |
| `preferences.dynamicImages[]` | array<object> | no |  |
| `preferences.emulateMode` | list | no | One of: ``, `print`, `screen`. |
| `preferences.flattenPdf` | boolean | no |  |
| `preferences.footer` | string | no |  |
| `preferences.format` | list | no | One of: `A3`, `A4`, `A5`, `Custom`, `Legal`, `Letter`, `Tabloid`. |
| `preferences.header` | string | no |  |
| `preferences.height` | number | no |  |
| `preferences.margin` | object | no |  |
| `preferences.orientation` | list | no | One of: `landscape`, `portrait`. |
| `preferences.outputFileName` | string | no |  |
| `preferences.outputType` | list | no | One of: `docx`, `html`, `jpeg`, `pdf`, `png`, `pptx`, `xlsx`. |
| `preferences.password` | string | no |  |
| `preferences.timezone` | string | no |  |
| `preferences.width` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docupilot API returns.

## Native endpoint

Through the native Docupilot API, this operation is `PUT /dashboard/api/v2/templates/{id}/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.


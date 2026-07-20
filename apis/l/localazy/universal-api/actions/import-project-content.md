# Localazy: Import Project Content

Imports localization files into a Localazy project.

```
POST https://connect.mindcloud.co/v1/universal/localazy/latest/actions/import-project-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/import-project-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "files[]": [
    {}
  ],
  "files[].name": "Ava Chen",
  "files[].content": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/import-project-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "files[]": [{}],
    "files[].name": "Ava Chen",
    "files[].content": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Localazy project id or slug. |
| `importAsNew` | boolean | no | Send imported translations to the review flow instead of making them current immediately. |
| `forceCurrent` | boolean | no | Overwrite existing current translations. |
| `filterSource` | boolean | no | Skip importing translations that match the source language text. Default: `true`. |
| `forceSource` | boolean | no | Overwrite the source language values in Localazy. |
| `files[]` | array<object> | yes | Files and localization content to import. |
| `files[].name` | string | yes | Filename shown in Localazy. |
| `files[].content` | object | yes | File content payload including type and language maps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Import job identifier returned by Localazy. |

## Native endpoint

Through the native Localazy API, this operation is `POST /projects/:projectId/import` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-project-content.md) for the provider-specific parameters and requirements.


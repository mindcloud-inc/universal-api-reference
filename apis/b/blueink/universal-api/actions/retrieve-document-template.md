# Blueink: Retrieve Document Template

Retrieves a document template from Blueink.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-document-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-document-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-document-template?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "defaultValue": "string",
          "editorRoles": [
            "string"
          ],
          "format": "string",
          "h": 1,
          "key": "string",
          "kind": "string",
          "label": "string",
          "page": 1,
          "vMax": 1,
          "vMin": 1,
          "vPattern": "string",
          "w": 1,
          "x": 1,
          "y": 1
        }
      ],
      "fileUrl": "https://example.com",
      "id": "string",
      "isShared": true,
      "name": "Ava Chen",
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].defaultValue` | string |  |
| `fields[].editorRoles[]` | string |  |
| `fields[].format` | string |  |
| `fields[].h` | number |  |
| `fields[].key` | string |  |
| `fields[].kind` | string |  |
| `fields[].label` | string |  |
| `fields[].page` | number |  |
| `fields[].vMax` | number |  |
| `fields[].vMin` | number |  |
| `fields[].vPattern` | string |  |
| `fields[].w` | number |  |
| `fields[].x` | number |  |
| `fields[].y` | number |  |
| `fileUrl` | string |  |
| `id` | string |  |
| `isShared` | boolean |  |
| `name` | string |  |
| `roles[]` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /templates/:templateId/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-document-template.md) for the provider-specific parameters and requirements.


# ArcSite: Import PDF to Project

Imports a PDF as drawings into an ArcSite project.

```
POST https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/import-pdf-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/import-pdf-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "fileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/import-pdf-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "fileUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The ID of the project. |
| `fileUrl` | string | yes | Publicly accessible PDF URL to import. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "drawings": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `drawings[].id` | string |  |

## Native endpoint

Through the native ArcSite API, this operation is `POST /projects/:projectId/import_pdf` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-pdf-to-project.md) for the provider-specific parameters and requirements.


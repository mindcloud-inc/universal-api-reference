# ArcSite: Get Drawing

Retrieves one drawing by ID from ArcSite.

```
GET https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-drawing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-drawing?connectionId=$CONNECTION_ID&drawingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "drawingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/get-drawing?${params}`, {
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
| `drawingId` | string | yes | The ID of the drawing. |
| `drawingVersionId` | string | no | The ID of the drawing version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dxfUrl": {},
      "id": "string",
      "name": "Ava Chen",
      "pdfUrl": "https://example.com",
      "pngUrl": "https://example.com",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dxfUrl` | object |  |
| `id` | string |  |
| `name` | string |  |
| `pdfUrl` | string |  |
| `pngUrl` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native ArcSite API, this operation is `GET /drawings/:drawingId` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drawing.md) for the provider-specific parameters and requirements.


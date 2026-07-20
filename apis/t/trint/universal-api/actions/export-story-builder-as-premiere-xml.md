# Trint: Export Story Builder as Premiere XML

Exports a Story Builder file as Premiere XML from Trint.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/export-story-builder-as-premiere-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/export-story-builder-as-premiere-xml?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/export-story-builder-as-premiere-xml?${params}`, {
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
| `fileId` | string | yes | The story builder file identifier to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `title` | string | Exported asset title. |
| `url` | string | Temporary download URL for the exported asset. |

## Native endpoint

Through the native Trint API, this operation is `GET /export/story-builder/project_xml/:fileId` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-story-builder-as-premiere-xml.md) for the provider-specific parameters and requirements.


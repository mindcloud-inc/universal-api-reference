# DatoCMS: Get Record Version



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record-version?connectionId=$CONNECTION_ID&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record-version?${params}`, {
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
| `versionId` | string | yes | Record version ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "summary": "string",
        "title": "string"
      },
      "id": "string",
      "meta": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "isCurrent": true,
        "isPublished": true,
        "isValid": true
      },
      "relationships": {
        "editor": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "item": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "itemType": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.summary` | string |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `meta.createdAt` | date |  |
| `meta.isCurrent` | boolean |  |
| `meta.isPublished` | boolean |  |
| `meta.isValid` | boolean |  |
| `relationships.editor.data.id` | string |  |
| `relationships.editor.data.type` | string |  |
| `relationships.item.data.id` | string |  |
| `relationships.item.data.type` | string |  |
| `relationships.itemType.data.id` | string |  |
| `relationships.itemType.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /versions/:versionId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-version.md) for the provider-specific parameters and requirements.


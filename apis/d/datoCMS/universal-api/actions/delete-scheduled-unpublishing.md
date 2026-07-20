# DatoCMS: Delete Scheduled Unpublishing



```
DELETE https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-scheduled-unpublishing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-scheduled-unpublishing?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-scheduled-unpublishing?${params}`, {
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
| `itemId` | string | yes | Record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "summary": "string",
        "summaryCopy1": "string",
        "summaryCopy2": "string",
        "title": "string"
      },
      "id": "string",
      "meta": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currentVersion": "string",
        "firstPublishedAt": "2026-05-07T12:00:00.000Z",
        "hasChildren": "string",
        "isCurrentVersionValid": true,
        "isPublishedVersionValid": "string",
        "isValid": true,
        "publicationScheduledAt": "string",
        "publishedAt": "string",
        "stage": "string",
        "status": "string",
        "unpublishingScheduledAt": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "relationships": {
        "creator": {
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
| `attributes.summaryCopy1` | string |  |
| `attributes.summaryCopy2` | string |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `meta.createdAt` | date |  |
| `meta.currentVersion` | string |  |
| `meta.firstPublishedAt` | date |  |
| `meta.hasChildren` | string |  |
| `meta.isCurrentVersionValid` | boolean |  |
| `meta.isPublishedVersionValid` | string |  |
| `meta.isValid` | boolean |  |
| `meta.publicationScheduledAt` | string |  |
| `meta.publishedAt` | string |  |
| `meta.stage` | string |  |
| `meta.status` | string |  |
| `meta.unpublishingScheduledAt` | string |  |
| `meta.updatedAt` | date |  |
| `relationships.creator.data.id` | string |  |
| `relationships.creator.data.type` | string |  |
| `relationships.itemType.data.id` | string |  |
| `relationships.itemType.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `DELETE /items/:itemId/scheduled-unpublishing` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scheduled-unpublishing.md) for the provider-specific parameters and requirements.


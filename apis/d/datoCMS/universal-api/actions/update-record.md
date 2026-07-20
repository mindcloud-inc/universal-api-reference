# DatoCMS: Update Record



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "LtUziyVcQpaAiV81ERJSMg",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "LtUziyVcQpaAiV81ERJSMg",
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | Example: `LtUziyVcQpaAiV81ERJSMg`. |
| `attributes` | object | yes | Default: `{}`. Example: `[object Object]`. |
| `attributes.image.uploadId` | string | no |  |
| `attributes.image.alt` | string | no |  |
| `attributes.image.title` | string | no |  |
| `attributes.category` | string | no |  |
| `attributes.content` | string | no |  |
| `attributes.image` | object | no |  |
| `attributes.title` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `relationships` | object | no | Relationship links for the record payload. Example: `[object Object]`. |
| `meta` | object | no | Record metadata block for status and workflow attributes. Example: `[object Object]`. |
| `skipItemValidation` | boolean | no | Skip required validator checks while updating the record. Example: `false`. |
| `skipInvalid` | boolean | no | Skip invalid records when processing update request. Example: `false`. |
| `relationships.itemType.data` | object | no |  |
| `relationships.itemType.data.type` | string | no |  |
| `relationships.itemType.data.id` | string | no |  |
| `relationships.creator.data` | object | no |  |
| `meta.createdAt` | string | no |  |
| `meta.currentVersion` | string | no |  |
| `meta.firstPublishedAt` | string | no |  |
| `meta.hasChildren` | boolean | no |  |
| `meta.isCurrentVersionValid` | boolean | no |  |
| `meta.isPublishedVersionValid` | boolean | no |  |
| `meta.isValid` | boolean | no |  |
| `meta.publicationScheduledAt` | string | no |  |
| `meta.publishedAt` | string | no |  |
| `meta.stage` | string | no |  |
| `meta.status` | string | no |  |
| `meta.unpublishingScheduledAt` | string | no |  |
| `meta.updatedAt` | string | no |  |
| `relationships.creator` | object | no |  |
| `relationships.itemType` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "meta": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `meta` | object |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `PUT /items/:itemId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.


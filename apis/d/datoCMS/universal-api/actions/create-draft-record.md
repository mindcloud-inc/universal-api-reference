# DatoCMS: Create Draft Record



```
POST https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-draft-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-draft-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemTypeId": "Ey1hk04gQ9ib4oyfQuFK5A",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-draft-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemTypeId": "Ey1hk04gQ9ib4oyfQuFK5A",
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemTypeId` | string | yes | Example: `Ey1hk04gQ9ib4oyfQuFK5A`. |
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
| `bodyId` | string | no | Optional custom ID for the new record. Example: `item_custom_id`. |
| `relationships` | object | no | Relationship links for the record payload. Example: `[object Object]`. |
| `meta` | object | no | Record metadata block for status and workflow attributes. Example: `[object Object]`. |
| `skipItemValidation` | boolean | no | Skip required validator checks while creating the record. Example: `false`. |
| `skipInvalid` | boolean | no | Skip invalid records when processing create request. Example: `false`. |
| `meta.createdAt` | string | no |  |
| `meta.currentVersion` | string | no |  |
| `meta.firstPublishedAt` | string | no |  |
| `meta.isCurrentVersionValid` | boolean | no |  |
| `meta.isPublishedVersionValid` | boolean | no |  |
| `meta.isValid` | boolean | no |  |
| `meta.publicationScheduledAt` | string | no |  |
| `meta.publishedAt` | string | no |  |
| `meta.status` | string | no |  |
| `meta.updatedAt` | string | no |  |

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
| `attributes` | object | Record attributes |
| `id` | string | Record ID |
| `meta` | object | Metadata |
| `relationships` | object | Related resources |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `POST /items` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-record.md) for the provider-specific parameters and requirements.


# Dukaan: Add Customer Tag

Adds a tag to a customer in Dukaan.

```
POST https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/add-customer-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/add-customer-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storeUuid": "your-store-uuid",
  "tag": "90198",
  "objectId": "21881957",
  "contentType": "storelead"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/add-customer-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storeUuid": "your-store-uuid",
    "tag": "90198",
    "objectId": "21881957",
    "contentType": "storelead"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeUuid` | string | yes | Dukaan store UUID from developer settings. Example: `your-store-uuid`. |
| `tag` | number | yes | Dukaan tag ID. Example: `90198`. |
| `objectId` | string | yes | Customer/store lead object ID to tag. Example: `21881957`. |
| `contentType` | string | yes | Dukaan content type for the tagged object. Default: `storelead`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "object_id": 1,
      "tag": 1,
      "tag_for": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_type` | string | Tagged object content type |
| `created_at` | date | Creation timestamp |
| `id` | number | Dukaan tag ID |
| `modified_at` | date | Last modified timestamp |
| `name` | string | Tag name |
| `object_id` | number | Tagged object ID |
| `tag` | number | Existing tag ID |
| `tag_for` | string | Tag target type |
| `uuid` | string | Dukaan tag UUID |

## Native endpoint

Through the native Dukaan API, this operation is `POST api/store/seller/:storeUuid/tags/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-customer-tag.md) for the provider-specific parameters and requirements.


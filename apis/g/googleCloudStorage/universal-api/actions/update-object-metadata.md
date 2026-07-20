# Google Cloud Storage: Update Object Metadata

Updates object metadata in Google Cloud Storage.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/update-object-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/update-object-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucket": "string",
  "object": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/update-object-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucket": "string",
    "object": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | list<string> | yes | Bucket name. |
| `object` | string | yes | Object name. |
| `metadata` | object | no | Custom object metadata object. |
| `contentType` | string | no | Object content type metadata. |
| `cacheControl` | string | no | Cache-Control directive for the object data. |
| `contentDisposition` | string | no | Content-Disposition value for the object data. |
| `contentEncoding` | string | no | Content-Encoding value for the object data. |
| `contentLanguage` | string | no | Content-Language value for the object data. |
| `customTime` | date | no | User-specified object timestamp in RFC 3339 format. |
| `eventBasedHold` | boolean | no | Whether the object is subject to an event-based hold. |
| `temporaryHold` | boolean | no | Whether the object is subject to a temporary hold. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `retention` | object | no | Object retention configuration. |
| `retention.mode` | list<string> | no | Object retention mode. One of: `Locked`, `Unlocked`. |
| `retention.retainUntilTime` | date | no | Earliest time the object can be deleted or replaced, in RFC 3339 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": "string",
      "contentType": "string",
      "generation": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "size": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `contentType` | string |  |
| `generation` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `size` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `PATCH /storage/v1/b/:bucket/o/:object` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-object-metadata.md) for the provider-specific parameters and requirements.


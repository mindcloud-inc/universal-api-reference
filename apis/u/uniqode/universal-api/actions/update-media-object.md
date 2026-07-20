# Uniqode: Update Media Object

Updates an existing media object in Uniqode.

```
PUT https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/update-media-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/update-media-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/update-media-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_type": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "folder": 1,
      "id": 1,
      "maintainer": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organization": 1,
      "s3_object_key": "string",
      "status": "string",
      "typeform_compatible": true,
      "typeform_url": "https://example.com",
      "url": "https://example.com",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_type` | string |  |
| `created` | date |  |
| `folder` | number |  |
| `id` | number |  |
| `maintainer` | number |  |
| `modified` | date |  |
| `name` | string |  |
| `organization` | number |  |
| `s3_object_key` | string |  |
| `status` | string |  |
| `typeform_compatible` | boolean |  |
| `typeform_url` | string |  |
| `url` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Uniqode API, this operation is `PUT /media/:mediaId/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-media-object.md) for the provider-specific parameters and requirements.


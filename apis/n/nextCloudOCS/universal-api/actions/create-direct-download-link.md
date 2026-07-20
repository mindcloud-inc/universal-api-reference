# Next Cloud OCS: Create Direct Download Link

Creates a new direct download link in Next Cloud OCS.

```
POST https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/create-direct-download-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/create-direct-download-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/create-direct-download-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | Nextcloud file ID for the direct download link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileId": "string",
      "message": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileId` | string |  |
| `message` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `POST /ocs/v2.php/apps/dav/api/v1/direct` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-download-link.md) for the provider-specific parameters and requirements.


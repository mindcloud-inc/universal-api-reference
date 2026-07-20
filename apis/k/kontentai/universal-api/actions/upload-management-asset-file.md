# Kontent.ai: Upload management asset file

Uploads an asset file to Kontent.ai.

```
POST https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upload-management-asset-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upload-management-asset-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upload-management-asset-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | File name to assign to the uploaded asset file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Uploaded file ID. |
| `url` | string | Uploaded file URL. |

## Native endpoint

Through the native Kontent.ai API, this operation is `POST https://manage.kontent.ai/v2/projects/:environment_id/files/:file_name` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-management-asset-file.md) for the provider-specific parameters and requirements.


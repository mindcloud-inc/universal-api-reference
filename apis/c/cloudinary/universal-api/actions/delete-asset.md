# Cloudinary: Delete Asset

Deletes an asset from your Cloudinary account.

```
DELETE https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-asset?connectionId=$CONNECTION_ID&publicId=string&resourceType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "resourceType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-asset?${params}`, {
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
| `publicId` | string | yes | The public ID to destroy. |
| `resourceType` | string | yes | The Cloudinary resource type, such as image, video, or raw. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Cloudinary API, this operation is `POST /:resource_type/destroy` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset.md) for the provider-specific parameters and requirements.


# Openlayer: Get Storage Download URL

Retrieves a storage download URL from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-storage-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-storage-download-url?connectionId=$CONNECTION_ID&storageUri=s3%3A%2F%2Fapi-openlayer-assets-us-west-2%2Fworkspaces%2Fb9ef2789-e1dd-4946-9ab0-189dcee20750%2Fusers%2F5e0d836f-f7a3-45db-bb5a-632f9e03aa8d%2Fuploads%2F1775742330-d2efa942%2Fmindcloud-openlayer-runtime.bin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storageUri": "s3://api-openlayer-assets-us-west-2/workspaces/b9ef2789-e1dd-4946-9ab0-189dcee20750/users/5e0d836f-f7a3-45db-bb5a-632f9e03aa8d/uploads/1775742330-d2efa942/mindcloud-openlayer-runtime.bin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-storage-download-url?${params}`, {
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
| `storageUri` | string | yes | Stored object URI. Default: `s3://api-openlayer-assets-us-west-2/workspaces/b9ef2789-e1dd-4946-9ab0-189dcee20750/users/5e0d836f-f7a3-45db-bb5a-632f9e03aa8d/uploads/1775742330-d2efa942/mindcloud-openlayer-runtime.bin`. |
| `workspaceId` | string | no | Workspace scope for the storage URL. Default: `b9ef2789-e1dd-4946-9ab0-189dcee20750`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /storage/presigned-url` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage-download-url.md) for the provider-specific parameters and requirements.


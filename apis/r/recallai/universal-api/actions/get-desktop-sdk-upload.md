# Recallai: Get Desktop SDK Upload

Retrieves a desktop SDK upload from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-desktop-sdk-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-desktop-sdk-upload?connectionId=$CONNECTION_ID&sdkUploadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sdkUploadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-desktop-sdk-upload?${params}`, {
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
| `sdkUploadId` | string | yes | Desktop SDK Upload ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "metadata": {},
      "recordingId": "string",
      "status": {},
      "uploadToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `recordingId` | string |  |
| `status` | object |  |
| `uploadToken` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `GET /api/v1/sdk_upload/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-desktop-sdk-upload.md) for the provider-specific parameters and requirements.


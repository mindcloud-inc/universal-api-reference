# Canva: Create URL Asset Upload Job

Creates a URL asset upload job in Canva.

```
POST https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-url-asset-upload-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-url-asset-upload-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "My Awesome Asset",
  "url": "https://example.com/my_asset_to_upload.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-url-asset-upload-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "My Awesome Asset",
    "url": "https://example.com/my_asset_to_upload.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A name for the asset. Example: `My Awesome Asset`. |
| `url` | string | yes | The publicly accessible internet URL of the file to import. Example: `https://example.com/my_asset_to_upload.jpg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "id": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.id` | string | Canva URL asset upload job ID. |
| `job.status` | string | Current job status. |

## Native endpoint

Through the native Canva API, this operation is `POST /v1/url-asset-uploads` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-url-asset-upload-job.md) for the provider-specific parameters and requirements.


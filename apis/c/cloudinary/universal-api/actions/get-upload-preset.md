# Cloudinary: Get Upload Preset

Retrieves an upload preset from Cloudinary.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-upload-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-upload-preset?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-upload-preset?${params}`, {
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
| `name` | string | yes | The upload preset name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "name": "Ava Chen",
      "settings": {},
      "unsigned": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_id` | string |  |
| `name` | string |  |
| `settings` | object |  |
| `unsigned` | boolean |  |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /upload_presets/:name` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-preset.md) for the provider-specific parameters and requirements.


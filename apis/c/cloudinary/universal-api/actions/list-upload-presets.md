# Cloudinary: List Upload Presets

Retrieves upload presets from your Cloudinary account.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-upload-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-upload-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-upload-presets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "presets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `presets` | array<object> | Upload presets returned by Cloudinary. |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /upload_presets` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-upload-presets.md) for the provider-specific parameters and requirements.


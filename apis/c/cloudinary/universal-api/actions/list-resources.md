# Cloudinary: List Resources

Retrieves resources from your Cloudinary account.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources?connectionId=$CONNECTION_ID&resourceType=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceType": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources?${params}`, {
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
| `resourceType` | string | yes | The Cloudinary resource type, such as image, video, or raw. |
| `type` | string | yes | The delivery type, such as upload, private, or authenticated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_cursor": "string",
      "resources": [
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
| `next_cursor` | string |  |
| `resources` | array<object> |  |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /resources/:resource_type/:type` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.


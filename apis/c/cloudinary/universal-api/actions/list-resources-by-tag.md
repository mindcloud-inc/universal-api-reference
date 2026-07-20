# Cloudinary: List Resources by Tag

Retrieves Cloudinary resources by tag value.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources-by-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources-by-tag?connectionId=$CONNECTION_ID&resourceType=string&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceType": "string",
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/list-resources-by-tag?${params}`, {
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
| `tag` | string | yes | The tag to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `resources` | array<object> |  |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /resources/:resource_type/tags/:tag` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources-by-tag.md) for the provider-specific parameters and requirements.


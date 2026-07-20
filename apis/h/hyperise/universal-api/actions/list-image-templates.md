# Hyperise: List Image Templates

Retrieves image templates from Hyperise.

```
GET https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-image-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-image-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-image-templates?${params}`, {
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
      "data": [
        {
          "baseUrl": "https://example.com",
          "createdAt": "string",
          "height": 1,
          "id": 1,
          "imageHash": "string",
          "imageUrl": "https://example.com",
          "name": "Ava Chen",
          "previewImage": "string",
          "updatedAt": "string",
          "width": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].baseUrl` | string |  |
| `data[].createdAt` | string |  |
| `data[].height` | number |  |
| `data[].id` | number |  |
| `data[].imageHash` | string |  |
| `data[].imageUrl` | string |  |
| `data[].name` | string |  |
| `data[].previewImage` | string |  |
| `data[].updatedAt` | string |  |
| `data[].width` | number |  |

## Native endpoint

Through the native Hyperise API, this operation is `GET /image-templates` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-image-templates.md) for the provider-specific parameters and requirements.


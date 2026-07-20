# LinkedIn: Get Image

Retrieves an image from LinkedIn.

```
GET https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-image?connectionId=$CONNECTION_ID&imageUrn=urn%253Ali%253Aimage%253AD4D10AQFS1_ExBi4C-w" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageUrn": "urn%3Ali%3Aimage%3AD4D10AQFS1_ExBi4C-w"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-image?${params}`, {
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
| `imageUrn` | string | yes | Example: `urn%3Ali%3Aimage%3AD4D10AQFS1_ExBi4C-w`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "owner": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `owner` | string |  |
| `status` | string |  |

## Native endpoint

Through the native LinkedIn API, this operation is `GET /rest/images/:imageUrn` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image.md) for the provider-specific parameters and requirements.


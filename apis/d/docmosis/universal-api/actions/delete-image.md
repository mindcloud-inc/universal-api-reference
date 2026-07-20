# Docmosis: Delete Image



```
DELETE https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/delete-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/delete-image?connectionId=$CONNECTION_ID&imageName%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageName[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/delete-image?${params}`, {
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
| `imageName[]` | array<string> | yes | Image name or names to delete, as documented by Docmosis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "longMsg": "string",
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `longMsg` | string | Detailed status message from Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the image delete request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /deleteImage` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-image.md) for the provider-specific parameters and requirements.


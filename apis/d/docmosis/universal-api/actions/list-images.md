# Docmosis: List Images



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/list-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/list-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/list-images?${params}`, {
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
| `folder` | string | no | Optional starting folder path. If omitted, all images are listed. |
| `includeSubFolders` | string | no | Whether to include images within subfolders. Defaults to true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageList": [
        {}
      ],
      "imageListStale": true,
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
| `imageList` | array<object> | Images returned for the requested folder scope. |
| `imageListStale` | boolean | Whether Docmosis considers the image list temporarily stale. |
| `longMsg` | string | Detailed status message from Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the image listing request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /listImages` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-images.md) for the provider-specific parameters and requirements.


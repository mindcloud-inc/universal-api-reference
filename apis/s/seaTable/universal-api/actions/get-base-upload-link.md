# SeaTable: Get Base Upload Link

Retrieves an upload link for a SeaTable base asset.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-upload-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-upload-link?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-upload-link?${params}`, {
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
      "fileRelativePath": "string",
      "imgRelativePath": "string",
      "parentPath": "string",
      "uploadLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileRelativePath` | string |  |
| `imgRelativePath` | string |  |
| `parentPath` | string |  |
| `uploadLink` | string |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api/v2.1/dtable/app-upload-link/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-base-upload-link.md) for the provider-specific parameters and requirements.

